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
ms.openlocfilehash: 26e227b4b1e8047ca962ca9e65b139bacae55e03
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41599991"
---
# <a name="manage-tickets-through-servicenow"></a><span data-ttu-id="bcfe0-105">Gérer les tickets via ServiceNow</span><span class="sxs-lookup"><span data-stu-id="bcfe0-105">Manage tickets through ServiceNow</span></span>

<span data-ttu-id="bcfe0-106">Le centre de sécurité Microsoft 365 est optimisé grâce à la capacité à créer et suivre en mode natif des tickets dans ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-106">Microsoft 365 security center is being enhanced with the ability to natively create and track tickets in ServiceNow.</span></span> <span data-ttu-id="bcfe0-107">Les administrateurs de la sécurité peuvent envoyer une action d’amélioration de la [note sécurisée Microsoft](microsoft-secure-score.md) directement à ServiceNow et créer un ticket.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-107">Security administrators can send a [Microsoft Secure Score](microsoft-secure-score.md) improvement action directly to ServiceNow and create a ticket.</span></span> <span data-ttu-id="bcfe0-108">Les tickets de gestion des modifications et de gestion des incidents peuvent être créés.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-108">Both incident management and change management tickets can be created.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bcfe0-109">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="bcfe0-109">Prerequisites</span></span>

<span data-ttu-id="bcfe0-110">Avoir accès au centre de sécurité Microsoft 365 et à une instance ServiceNow avec :</span><span class="sxs-lookup"><span data-stu-id="bcfe0-110">Have access to the Microsoft 365 security center and a ServiceNow instance with:</span></span>  

* <span data-ttu-id="bcfe0-111">Kingston ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="bcfe0-111">Kingston or higher version</span></span>
* <span data-ttu-id="bcfe0-112">Disposer des informations d’identification d’administrateur AIM</span><span class="sxs-lookup"><span data-stu-id="bcfe0-112">Have admin HI credentials</span></span>
* <span data-ttu-id="bcfe0-113">Disposer des privilèges d’administrateur sur l’instance de votre fournisseur cible</span><span class="sxs-lookup"><span data-stu-id="bcfe0-113">Have admin privileges on your target vendor instance</span></span>

<span data-ttu-id="bcfe0-114">ServiceNow recommande que les utilisateurs conservent les paramètres par défaut dans votre instance de ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-114">ServiceNow recommends that users keep default settings in your ServiceNow instance.</span></span> <span data-ttu-id="bcfe0-115">Les personnalisations peuvent entraîner des erreurs lors de la fin de la liste de vérification de l’installation et de l’intégration avec le centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-115">Having customizations could cause errors when completing the installation checklist and integration with the Microsoft 365 security center.</span></span>

## <a name="data-exchange"></a><span data-ttu-id="bcfe0-116">Échange de données</span><span class="sxs-lookup"><span data-stu-id="bcfe0-116">Data exchange</span></span>

<span data-ttu-id="bcfe0-117">Lorsque vous connectez le centre de sécurité Microsoft 365 à ServiceNow, Microsoft reçoit les données supplémentaires suivantes :</span><span class="sxs-lookup"><span data-stu-id="bcfe0-117">When you connect the Microsoft 365 security center to ServiceNow, Microsoft receives the following additional data:</span></span>

* <span data-ttu-id="bcfe0-118">Nom de l’instance ServiceNow</span><span class="sxs-lookup"><span data-stu-id="bcfe0-118">ServiceNow instance name</span></span>
* <span data-ttu-id="bcfe0-119">ID client ServiceNow</span><span class="sxs-lookup"><span data-stu-id="bcfe0-119">ServiceNow client ID</span></span>
* <span data-ttu-id="bcfe0-120">Clé secrète client ServiceNow</span><span class="sxs-lookup"><span data-stu-id="bcfe0-120">ServiceNow client secret</span></span>
* <span data-ttu-id="bcfe0-121">Jetons d’accès ServiceNow & d’actualisation</span><span class="sxs-lookup"><span data-stu-id="bcfe0-121">ServiceNow access & refresh tokens</span></span>

<span data-ttu-id="bcfe0-122">Lorsque vous créez un ticket ServiceNow à partir du centre de sécurité Microsoft 365, les données suivantes sont envoyées à ServiceNow :</span><span class="sxs-lookup"><span data-stu-id="bcfe0-122">When you create a ServiceNow ticket from the Microsoft 365 security center, the following data is sent to ServiceNow:</span></span>

* <span data-ttu-id="bcfe0-123">ID d’utilisateur qui initie la création du ticket</span><span class="sxs-lookup"><span data-stu-id="bcfe0-123">User ID that initiates the ticket creation</span></span>
* <span data-ttu-id="bcfe0-124">Nom de la tâche</span><span class="sxs-lookup"><span data-stu-id="bcfe0-124">Task name</span></span>
* <span data-ttu-id="bcfe0-125">Description de la tâche</span><span class="sxs-lookup"><span data-stu-id="bcfe0-125">Task description</span></span>
* <span data-ttu-id="bcfe0-126">Priority</span><span class="sxs-lookup"><span data-stu-id="bcfe0-126">Priority</span></span>
* <span data-ttu-id="bcfe0-127">Date d’échéance</span><span class="sxs-lookup"><span data-stu-id="bcfe0-127">Due date</span></span>
* <span data-ttu-id="bcfe0-128">Source de recommandation (recommandation de l’utilisateur ou recommandation de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bcfe0-128">Recommendation source (User recommendation or Microsoft recommendation)</span></span>
* <span data-ttu-id="bcfe0-129">Catégorie de recommandation (périphériques, données, applications, identité, infrastructure)</span><span class="sxs-lookup"><span data-stu-id="bcfe0-129">Recommendation category (Devices, Data, Apps, Identity, Infrastructure)</span></span>

## <a name="connect-microsoft-365-security-center-to-servicenow"></a><span data-ttu-id="bcfe0-130">Connecter le centre de sécurité Microsoft 365 à ServiceNow</span><span class="sxs-lookup"><span data-stu-id="bcfe0-130">Connect Microsoft 365 security center to ServiceNow</span></span>

<span data-ttu-id="bcfe0-131">Accédez à la page d’accueil du centre de sécurité Microsoft 365 pour afficher la carte de connexion ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-131">Navigate to the Microsoft 365 security center home page to see the ServiceNow connection card.</span></span>

![Utilisez-vous ServiceNow](../images/do-you-use-servicenow-250.png)

<span data-ttu-id="bcfe0-133">Sélectionnez « se connecter à ServiceNow » pour accéder à la page de configuration de ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-133">Select "Connect to ServiceNow" to go to the ServiceNow setup page.</span></span> <span data-ttu-id="bcfe0-134">Suivez les instructions pour autoriser l’application Connecteur Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-134">Follow the instructions to authorize the Microsoft 365 Connector app.</span></span>

> [!NOTE]
> <span data-ttu-id="bcfe0-135">Avant d’autoriser la connexion entre le centre de sécurité Microsoft 365 et ServiceNow, veillez à utiliser le nom d’utilisateur et le mot de passe d’intégration que vous avez créés lors des étapes d’installation.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-135">Before you authorize the connection between Microsoft 365 security center and ServiceNow, make sure you use the integration user login and password you created in the installation steps.</span></span> <span data-ttu-id="bcfe0-136">N’utilisez pas vos informations d’identification personnelles.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-136">Do not use your personal credentials.</span></span>

<span data-ttu-id="bcfe0-137">Une fois que vous avez suivi les instructions et autorisé la connexion, consultez l’état de la connexion sur la page de connexion du centre de sécurité Microsoft 365 et dans l’expérience de l’application ServiceNow Microsoft 365 Ticketing Connector.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-137">After you have followed the directions and authorizing the connection, view the connection status on both the Microsoft 365 security center connection page and in the ServiceNow Microsoft 365 Ticketing Connector App experience.</span></span> <span data-ttu-id="bcfe0-138">Vous êtes maintenant prêt à commencer à créer des tâches !</span><span class="sxs-lookup"><span data-stu-id="bcfe0-138">Now you are all set to start creating tasks!</span></span>

## <a name="create-a-task-and-share-it-to-servicenow"></a><span data-ttu-id="bcfe0-139">Créer une tâche et la partager avec ServiceNow</span><span class="sxs-lookup"><span data-stu-id="bcfe0-139">Create a task and share it to ServiceNow</span></span>

<span data-ttu-id="bcfe0-140">Une fois l’intégration configurée, créez des tâches ServiceNow basées sur des actions d’amélioration spécifiques de Microsoft Secure score.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-140">Once the integration is set up, create ServiceNow tasks based on specific Microsoft Secure Score improvement actions.</span></span> <span data-ttu-id="bcfe0-141">Accédez à une action d’amélioration dans le score de sécurité dans le portail du centre de sécurité Microsoft 365, puis sélectionnez l’icône « partager ».</span><span class="sxs-lookup"><span data-stu-id="bcfe0-141">Go to any improvement action in Secure Score in the Microsoft 365 security center portal, and select the “share” icon.</span></span> <span data-ttu-id="bcfe0-142">L’une des options de liste déroulante est ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-142">One of the dropdown options is ServiceNow.</span></span>

![Partage ServiceNow dans le score de sécurité](../images/servicenow-share.png)

<span data-ttu-id="bcfe0-144">Une tâche est générée, dans laquelle vous pouvez définir la priorité et modifier le nom, la description ou la date d’échéance.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-144">A task is generated where you can set the priority and edit the name, description, or due date.</span></span> <span data-ttu-id="bcfe0-145">Une fois que tous les champs obligatoires sont renseignés, envoyez la tâche à ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-145">Once all the required fields are filled in, send the task to ServiceNow.</span></span>

<span data-ttu-id="bcfe0-146">La tâche est visible dans ServiceNow en tant que demande de modification de la configuration et de la sécurité de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-146">The task is visible in ServiceNow as a Microsoft 365 Security and Configuration Change Request.</span></span>

## <a name="track-tickets"></a><span data-ttu-id="bcfe0-147">Suivre les tickets</span><span class="sxs-lookup"><span data-stu-id="bcfe0-147">Track tickets</span></span>

<span data-ttu-id="bcfe0-148">Une fois que les tickets de gestion des modifications et de gestion des incidents ont été créés, ils s’affichent sur des cartes dans la page d’accueil du centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-148">Once ServiceNow change management and incident management tickets have been created, they are displayed on cards in the Microsoft 365 security center home page.</span></span> <span data-ttu-id="bcfe0-149">À partir de ces cartes, vous pouvez créer un ticket, afficher tous les tickets ou gérer la configuration de ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-149">From these cards, you can create a ticket, view all tickets, or manage the ServiceNow configuration.</span></span>

![Tickets de gestion des modifications ServiceNow](../images/change-management-375.png)  ![Tickets de gestion des incidents ServiceNow](../images/incident-management-375.png)

<span data-ttu-id="bcfe0-152">Pour reconfigurer ou gérer votre intégration ServiceNow dans le centre de sécurité Microsoft 365, sélectionnez **gérer la configuration de ServiceNow** sur l’une des cartes.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-152">To re-provision or manage your ServiceNow integration in the Microsoft 365 security center, select **Manage ServiceNow configuration** on either of the cards.</span></span> <span data-ttu-id="bcfe0-153">À partir de là, supprimez la connexion ServiceNow actuelle et personnalisez les noms d’état des tickets.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-153">From there, remove the current ServiceNow connection and customize ticket state names.</span></span>

<span data-ttu-id="bcfe0-154">Avec les tickets ServiceNow visibles dans le centre de sécurité Microsoft 365, vos tâches vivent à un endroit où elles peuvent être suivies et traitées parallèlement à vos autres éléments de tableau de bord de sécurité.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-154">With ServiceNow tickets visible in the Microsoft 365 security center, your tasks live in a place where they can be tracked and acted upon alongside your other security dashboard items.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="bcfe0-155">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="bcfe0-155">Troubleshooting</span></span>

### <a name="you-receive-an-error-in-the-first-step-of-the-installation-checklist-oauth-creation"></a><span data-ttu-id="bcfe0-156">Vous recevez une erreur dans la première étape de la liste de vérification de l’installation (création OAuth)</span><span class="sxs-lookup"><span data-stu-id="bcfe0-156">You receive an error in the first step of the installation checklist (OAuth creation)</span></span>

<span data-ttu-id="bcfe0-157">**Message d’erreur**: l’opération de lecture sur « oauth_entity » de l’étendue « x_mioms_m365ticket » a été refusée en raison de la stratégie d’accès aux étendues de la table</span><span class="sxs-lookup"><span data-stu-id="bcfe0-157">**Error Message**: Read operation against 'oauth_entity' from scope 'x_mioms_m365ticket' has been refused due to the table's cross-scope access policy</span></span>

<span data-ttu-id="bcfe0-158">L’application part du principe que n’importe quel administrateur de l’instance de ServiceNow peut créer et lire des entités OAuth.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-158">The app assumes any admin on the ServiceNow instance can create and read OAuth entities.</span></span> <span data-ttu-id="bcfe0-159">Cette erreur peut être due à une personnalisation sur votre instance de ServiceNow, ce qui limite les personnes autorisées à créer/lire des entités OAuth.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-159">This error could be caused due to a customization on your instance of ServiceNow, which restricts who can create/read OAuth entities.</span></span>

<span data-ttu-id="bcfe0-160">**ServiceNow recommande que les utilisateurs conservent les fonctionnalités par défaut.**</span><span class="sxs-lookup"><span data-stu-id="bcfe0-160">**ServiceNow recommends that users keep default functionality.**</span></span>

<span data-ttu-id="bcfe0-161">Définissez les configurations des tables « registres des applications » sur par défaut :</span><span class="sxs-lookup"><span data-stu-id="bcfe0-161">Set the “application registries” table configurations to default:</span></span>

* <span data-ttu-id="bcfe0-162">Label = registres de l’application</span><span class="sxs-lookup"><span data-stu-id="bcfe0-162">Label = Application Registeries</span></span>
* <span data-ttu-id="bcfe0-163">Nom = oauth_entity</span><span class="sxs-lookup"><span data-stu-id="bcfe0-163">Name = oauth_entity</span></span>
* <span data-ttu-id="bcfe0-164">Accessible à partir de = toutes les étendues d’application</span><span class="sxs-lookup"><span data-stu-id="bcfe0-164">Accessible from = All application scopes</span></span>
* <span data-ttu-id="bcfe0-165">Lecture possible = case à cocher activée</span><span class="sxs-lookup"><span data-stu-id="bcfe0-165">Can read = check box selected</span></span>

### <a name="how-to-validate-the-oauth-entity-created-for-microsoft-365-security--compliance-connector"></a><span data-ttu-id="bcfe0-166">Procédure de validation de l’entité OAuth créée pour Microsoft 365 Security & Compliance Connector</span><span class="sxs-lookup"><span data-stu-id="bcfe0-166">How to validate the OAuth entity created for Microsoft 365 Security & Compliance connector</span></span>

<span data-ttu-id="bcfe0-167">Accédez à la table des registres des applications (**Menu > système oauth > application Registry**) dans ServiceNow et recherchez l’entité OAuth créée par vous, avec le nom que vous lui avez attribué.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-167">Go to application registries table (**Menu > System OAuth > Application Registry**) in ServiceNow and find the OAuth entity created by you, with the name that you assigned it.</span></span>

### <a name="logging-in-as-the-integration-user"></a><span data-ttu-id="bcfe0-168">Connexion en tant qu’utilisateur de l’intégration</span><span class="sxs-lookup"><span data-stu-id="bcfe0-168">Logging in as the integration user</span></span>

<span data-ttu-id="bcfe0-169">Avant d’autoriser la connexion entre le centre de sécurité Microsoft 365 et ServiceNow, veillez à utiliser le nom d’utilisateur et le mot de passe d’intégration que vous avez créés lors des étapes d’installation.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-169">Before you authorize the connection between Microsoft 365 security center and ServiceNow, make sure you use the integration user login and password you created in the installation steps.</span></span> <span data-ttu-id="bcfe0-170">N’utilisez pas vos informations d’identification personnelles.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-170">Do not use your personal credentials.</span></span>

1. <span data-ttu-id="bcfe0-171">Accédez à la page Authorization (autorisation) dans ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-171">Go the authorization page in ServiceNow.</span></span>
2. <span data-ttu-id="bcfe0-172">Si vous êtes connecté avec vos informations d’identification personnelles, sélectionnez le lien qui ne se trouve **pas** dans le coin supérieur droit.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-172">If you are signed in with your personal credentials, select the **Not You** link in the upper right-hand corner.</span></span>
3. <span data-ttu-id="bcfe0-173">Connectez-vous à ServiceNow en tant qu’utilisateur d’intégration que vous avez créé précédemment à partir de la liste de vérification d’installation.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-173">Log in to ServiceNow as the integration user you created previously from the installation checklist.</span></span>  
4. <span data-ttu-id="bcfe0-174">Sélectionnez **autoriser** dans la page ServiceNow pour demander si le connecteur sécurité + conformité peut se connecter à votre compte ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-174">Select **Allow** in the ServiceNow page that asks whether the Security + Compliance Connector can connect to your ServiceNow account.</span></span>
5. <span data-ttu-id="bcfe0-175">Suivez les étapes de configuration.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-175">Proceed with the setup steps.</span></span>

### <a name="how-to-validate-the-integration-user-created-with-the-installation-checklist-for-microsoft-365-security--compliance-connector"></a><span data-ttu-id="bcfe0-176">Procédure de validation de l’utilisateur d’intégration créé avec la liste de vérification d’installation pour le connecteur de sécurité & conformité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="bcfe0-176">How to validate the Integration User created with the installation checklist for Microsoft 365 Security & Compliance connector</span></span>

<span data-ttu-id="bcfe0-177">Accédez à la table utilisateurs **(Menu > l’administration des utilisateurs > les utilisateurs**) dans ServiceNow et recherchez l’utilisateur d’intégration que vous avez créé, avec le nom que vous lui avez attribué.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-177">Go to Users Table **(Menu > User Administration > Users**) in ServiceNow and find the Integration user created by you, with the name that you assigned it.</span></span>

### <a name="your-company-has-single-sign-on-enabled-which-prevents-you-from-connecting-to-servicenow-through-the-microsoft-365-security-center"></a><span data-ttu-id="bcfe0-178">Votre entreprise a activé l’authentification unique, ce qui vous empêche de vous connecter à ServiceNow via le centre de sécurité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="bcfe0-178">Your company has single sign-on enabled which prevents you from connecting to ServiceNow through the Microsoft 365 security center</span></span>

<span data-ttu-id="bcfe0-179">Si votre entreprise a activé l’authentification unique et que vous recevez une erreur ou si la connexion échoue, suivez l’une des deux solutions.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-179">If your company has enabled single sign-on and you receive an error or login is unsuccessful, follow one of the two solutions.</span></span>

#### <a name="log-into-servicenow-as-the-integration-user"></a><span data-ttu-id="bcfe0-180">Connectez-vous à ServiceNow en tant qu’utilisateur d’intégration.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-180">Log into ServiceNow as the integration user</span></span>

1. <span data-ttu-id="bcfe0-181">Revenez à la page autorisation dans ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-181">Navigate back to the authorization page in ServiceNow.</span></span>
2. <span data-ttu-id="bcfe0-182">Sélectionnez le lien qui **n’est pas** dans le coin supérieur droit.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-182">Select the **Not You** link in the upper right-hand corner.</span></span>
3. <span data-ttu-id="bcfe0-183">Connectez-vous à ServiceNow en tant qu’utilisateur d’intégration que vous avez créé précédemment à partir de la liste de vérification d’installation.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-183">Log in to ServiceNow as the integration user you created previously from the installation checklist.</span></span>  
4. <span data-ttu-id="bcfe0-184">Sélectionnez **autoriser** dans la page ServiceNow pour demander si le connecteur sécurité + conformité peut se connecter à votre compte ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-184">Select **Allow** in the ServiceNow page that asks whether the Security + Compliance Connector can connect to your ServiceNow account.</span></span>
5. <span data-ttu-id="bcfe0-185">Suivez les étapes de configuration.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-185">Proceed with the setup steps.</span></span>

#### <a name="create-a-security-admin-user"></a><span data-ttu-id="bcfe0-186">Créer un utilisateur d’administrateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="bcfe0-186">Create a security admin user</span></span>

1. <span data-ttu-id="bcfe0-187">Créez un utilisateur avec des privilèges d’administrateur de sécurité dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-187">Create a user with security admin privileges in Azure Active Directory.</span></span> <span data-ttu-id="bcfe0-188">L’utilisateur doit avoir les mêmes nom et adresse de messagerie que l’utilisateur d’intégration que vous avez créé à partir de la liste de vérification d’installation.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-188">The user needs to have the same name and email address as the integration user you created from the Installation Checklist.</span></span> <span data-ttu-id="bcfe0-189">Vous pouvez supprimer le rôle d’administrateur de sécurité une fois la connexion et la connexion terminées.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-189">You can remove the security admin role once login and connection has been completed.</span></span>
2. <span data-ttu-id="bcfe0-190">Connectez-vous au centre de sécurité Microsoft 365 en tant qu’utilisateur et suivez les étapes de configuration.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-190">Log in to the Microsoft 365 security center as this user and follow the setup steps.</span></span>

### <a name="installation-is-complete-but-dont-see-tickets-and-cant-share"></a><span data-ttu-id="bcfe0-191">L’installation est terminée, mais ne vois pas les tickets et ne peut pas partager</span><span class="sxs-lookup"><span data-stu-id="bcfe0-191">Installation is complete but don't see tickets and can't share</span></span>

<span data-ttu-id="bcfe0-192">Si les étapes d’installation et de configuration sont terminées, mais que vous ne voyez pas les cartes ServiceNow sur la page d’accueil et que vous ne pouvez pas partager de ServiceNow à partir du score de sécurité https://security.microsoft.com/ticketProvisioningMicrosoft, vérifiez l’état de la page de mise en service sur.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-192">If the installation and setup steps have been completed, but you don't see the ServiceNow cards on the home page and can't share to ServiceNow from Microsoft Secure Score, check the status of the provisioning page at https://security.microsoft.com/ticketProvisioning.</span></span> <span data-ttu-id="bcfe0-193">Sélectionnez **autoriser** et revenir à la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-193">Select **Authorize** and return to the home page.</span></span> <span data-ttu-id="bcfe0-194">Les cartes doivent apparaître.</span><span class="sxs-lookup"><span data-stu-id="bcfe0-194">The cards should appear.</span></span>

