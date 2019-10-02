---
title: Créer et suivre des tickets via ServiceNow
description: Le centre de sécurité Microsoft 365 est optimisé grâce à la capacité à créer et suivre en mode natif des tickets dans ServiceNow. Cela permet aux administrateurs de sécurité d’envoyer une recommandation de score sécurisé directement à ServiceNow et de créer un ticket.
keywords: sécurité, Microsoft 365, M365, Secure score, Security Center, ServiceNow, tickets, Tasks
ms.prod: w10
ms.mktglfcycl: deploy
ms.localizationpriority: medium
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
ms.openlocfilehash: b0b8cda81bb6cec3958e7b2a758da191d803a0ed
ms.sourcegitcommit: acf29701bfba3e4843e49a79fde012f3c7a7024a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/01/2019
ms.locfileid: "37350328"
---
# <a name="manage-tickets-through-servicenow"></a><span data-ttu-id="d6223-105">Gérer les tickets via ServiceNow</span><span class="sxs-lookup"><span data-stu-id="d6223-105">Manage tickets through ServiceNow</span></span>

<span data-ttu-id="d6223-106">Le centre de sécurité Microsoft 365 est optimisé grâce à la capacité à créer et suivre en mode natif des tickets dans ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="d6223-106">Microsoft 365 security center is being enhanced with the ability to natively create and track tickets in ServiceNow.</span></span> <span data-ttu-id="d6223-107">Cela permet aux administrateurs de sécurité d’envoyer une action d’amélioration de la [note sécurisée Microsoft](microsoft-secure-score.md) directement à ServiceNow et de créer un ticket.</span><span class="sxs-lookup"><span data-stu-id="d6223-107">This allows security administrators to send a [Microsoft Secure Score](microsoft-secure-score.md) improvement action directly to ServiceNow and create a ticket.</span></span> <span data-ttu-id="d6223-108">Les tickets de gestion des modifications et de gestion des incidents peuvent être créés.</span><span class="sxs-lookup"><span data-stu-id="d6223-108">Both incident management and change management tickets can be created.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d6223-109">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="d6223-109">Prerequisites</span></span>

<span data-ttu-id="d6223-110">Avoir accès au centre de sécurité Microsoft 365 et à une instance ServiceNow avec :</span><span class="sxs-lookup"><span data-stu-id="d6223-110">Have access to the Microsoft 365 security center and a ServiceNow instance with:</span></span>  

* <span data-ttu-id="d6223-111">Kingston ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="d6223-111">Kingston or higher version</span></span>
* <span data-ttu-id="d6223-112">Disposer des informations d’identification d’administrateur AIM</span><span class="sxs-lookup"><span data-stu-id="d6223-112">Have admin HI credentials</span></span>
* <span data-ttu-id="d6223-113">Disposer des privilèges d’administrateur sur l’instance de votre fournisseur cible</span><span class="sxs-lookup"><span data-stu-id="d6223-113">Have admin privileges on your target vendor instance</span></span>

<span data-ttu-id="d6223-114">ServiceNow recommande aux utilisateurs de conserver les paramètres par défaut dans votre instance de ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="d6223-114">ServiceNow recommends users keep out of the box settings (default) in your ServiceNow instance.</span></span>  <span data-ttu-id="d6223-115">Le fait d’avoir des personnalisations peut provoquer des erreurs lors de la vérification de la liste de contrôle et de l’intégration avec le centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d6223-115">Having customizations could cause errors in completing the installation checklist and integration with the Microsoft 365 security center.</span></span>

## <a name="data-exchange"></a><span data-ttu-id="d6223-116">Échange de données</span><span class="sxs-lookup"><span data-stu-id="d6223-116">Data exchange</span></span>

<span data-ttu-id="d6223-117">Lorsque vous connectez le centre de sécurité Microsoft 365 à ServiceNow, Microsoft reçoit les données supplémentaires suivantes :</span><span class="sxs-lookup"><span data-stu-id="d6223-117">When you connect the Microsoft 365 security center to ServiceNow, Microsoft will be receiving the following additional data:</span></span>

* <span data-ttu-id="d6223-118">Nom de l’instance ServiceNow</span><span class="sxs-lookup"><span data-stu-id="d6223-118">ServiceNow instance name</span></span>
* <span data-ttu-id="d6223-119">ID client ServiceNow</span><span class="sxs-lookup"><span data-stu-id="d6223-119">ServiceNow client ID</span></span>
* <span data-ttu-id="d6223-120">Clé secrète client ServiceNow</span><span class="sxs-lookup"><span data-stu-id="d6223-120">ServiceNow client secret</span></span>
* <span data-ttu-id="d6223-121">Jetons d’accès ServiceNow & d’actualisation</span><span class="sxs-lookup"><span data-stu-id="d6223-121">ServiceNow access & refresh tokens</span></span>

<span data-ttu-id="d6223-122">Lorsque vous créez un ticket ServiceNow à partir du centre de sécurité Microsoft 365, les données suivantes sont envoyées à ServiceNow :</span><span class="sxs-lookup"><span data-stu-id="d6223-122">When you create a ServiceNow ticket from the Microsoft 365 security center the following data is sent to ServiceNow:</span></span>

* <span data-ttu-id="d6223-123">ID d’utilisateur qui initie la création du ticket</span><span class="sxs-lookup"><span data-stu-id="d6223-123">User ID that initiates the ticket creation</span></span>
* <span data-ttu-id="d6223-124">Nom de la tâche</span><span class="sxs-lookup"><span data-stu-id="d6223-124">Task name</span></span>
* <span data-ttu-id="d6223-125">Description de la tâche</span><span class="sxs-lookup"><span data-stu-id="d6223-125">Task description</span></span>
* <span data-ttu-id="d6223-126">Priority</span><span class="sxs-lookup"><span data-stu-id="d6223-126">Priority</span></span>
* <span data-ttu-id="d6223-127">Date d’échéance</span><span class="sxs-lookup"><span data-stu-id="d6223-127">Due date</span></span>
* <span data-ttu-id="d6223-128">Source de recommandation (recommandation de l’utilisateur ou recommandation de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d6223-128">Recommendation source (User recommendation or Microsoft recommendation)</span></span>
* <span data-ttu-id="d6223-129">Catégorie de recommandation (périphériques, données, applications, identité, infrastructure)</span><span class="sxs-lookup"><span data-stu-id="d6223-129">Recommendation category (Devices, Data, Apps, Identity, Infrastructure)</span></span>

## <a name="connect-microsoft-365-security-center-to-servicenow"></a><span data-ttu-id="d6223-130">Connecter le centre de sécurité Microsoft 365 à ServiceNow</span><span class="sxs-lookup"><span data-stu-id="d6223-130">Connect Microsoft 365 security center to ServiceNow</span></span>

<span data-ttu-id="d6223-131">Accédez à la page d’accueil du centre de sécurité Microsoft 365, dans laquelle vous verrez une carte vous demandant si vous utilisez ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="d6223-131">Navigate to the Microsoft 365 security center home page, where you will see a card asking if you use ServiceNow.</span></span>

![Utilisez-vous ServiceNow](../images/do-you-use-servicenow-250.png)

<span data-ttu-id="d6223-133">À partir de là, vous serez redirigé vers la page de configuration de ServiceNow, dans laquelle vous suivrez les instructions pour autoriser l’application de connecteur Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d6223-133">From there you will be sent to the ServiceNow set up page where you'll follow the instructions to authorize the Microsoft 365 Connector app.</span></span>

<span data-ttu-id="d6223-134">Lors de l’autorisation de la connexion entre le centre de sécurité Microsoft 365 et ServiceNow, veillez à utiliser la connexion utilisateur et le mot de passe d’intégration que vous avez créés lors de la procédure d’installation et pas vos informations d’identification personnelles.</span><span class="sxs-lookup"><span data-stu-id="d6223-134">When authorizing the connection between Microsoft 365 security center and ServiceNow, make sure you use the integration user login and password you created in the installation steps and not your personal credentials.</span></span>

<span data-ttu-id="d6223-135">Après avoir suivi les instructions et autorisé la connexion, vous pouvez afficher l’état de la connexion sur la page de connexion du centre de sécurité Microsoft 365 et dans l’expérience de l’application ServiceNow Microsoft 365 Ticketing Connector.</span><span class="sxs-lookup"><span data-stu-id="d6223-135">After following the directions and authorizing the connection, you can view the connection status on both the Microsoft 365 security center connection page and in the ServiceNow Microsoft 365 Ticketing Connector App experience.</span></span> <span data-ttu-id="d6223-136">Vous êtes maintenant prêt à commencer à créer des tâches !</span><span class="sxs-lookup"><span data-stu-id="d6223-136">Now you are all set to start creating tasks!</span></span>

## <a name="create-a-task-and-share-it-to-servicenow"></a><span data-ttu-id="d6223-137">Créer une tâche et la partager avec ServiceNow</span><span class="sxs-lookup"><span data-stu-id="d6223-137">Create a task and share it to ServiceNow</span></span>

<span data-ttu-id="d6223-138">Une fois l’intégration configurée, vous pouvez créer des tâches ServiceNow basées sur des actions d’amélioration spécifiques de Microsoft Secure score.</span><span class="sxs-lookup"><span data-stu-id="d6223-138">Once the integration is set up, you can create ServiceNow tasks based on specific Microsoft Secure Score improvement actions.</span></span> <span data-ttu-id="d6223-139">Accédez à une action d’amélioration dans le score de sécurité dans le portail du centre de sécurité Microsoft 365, puis sélectionnez l’icône « partager ».</span><span class="sxs-lookup"><span data-stu-id="d6223-139">Go to any improvement action in Secure Score in the Microsoft 365 security center portal, and select the “share” icon.</span></span> <span data-ttu-id="d6223-140">L’une des options de liste déroulante est ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="d6223-140">One of the dropdown options is ServiceNow.</span></span>

![Partage ServiceNow dans le score de sécurité](../images/servicenow-share.png)

<span data-ttu-id="d6223-142">Une tâche est ensuite générée, dans laquelle vous pouvez définir la priorité et modifier le nom, la description ou la date d’échéance.</span><span class="sxs-lookup"><span data-stu-id="d6223-142">A task will then be generated where you can set the priority and edit the name, description, or due date.</span></span> <span data-ttu-id="d6223-143">Une fois que tous les champs obligatoires sont renseignés, vous pouvez envoyer la tâche à ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="d6223-143">Once all the required fields are filled in, you can send the task to ServiceNow.</span></span>

<span data-ttu-id="d6223-144">La tâche est visible dans ServiceNow en tant que demande de modification de la configuration et de la sécurité de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d6223-144">The task will be visible in ServiceNow as a Microsoft 365 Security and Configuration Change Request.</span></span>

## <a name="track-tickets"></a><span data-ttu-id="d6223-145">Suivre les tickets</span><span class="sxs-lookup"><span data-stu-id="d6223-145">Track tickets</span></span>

<span data-ttu-id="d6223-146">Une fois que les tickets de gestion des modifications et de gestion des incidents ont été créés, ils s’afficheront sur les cartes dans la page d’accueil du centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d6223-146">Once ServiceNow change management and incident management tickets have been created, they will be displayed on cards in the Microsoft 365 security center home page.</span></span> <span data-ttu-id="d6223-147">À partir de ces cartes, vous pouvez créer un ticket, afficher tous les tickets ou gérer la configuration de ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="d6223-147">From these cards, you can create a ticket, view all tickets, or manage the ServiceNow configuration.</span></span>

![Tickets de gestion des modifications ServiceNow](../images/change-management-375.png)  ![Tickets de gestion des incidents ServiceNow](../images/incident-management-375.png)

<span data-ttu-id="d6223-150">Pour reconfigurer ou gérer votre intégration ServiceNow dans le centre de sécurité Microsoft 365, sélectionnez **gérer la configuration de ServiceNow** sur l’une des cartes.</span><span class="sxs-lookup"><span data-stu-id="d6223-150">To re-provision or manage your ServiceNow integration in the Microsoft 365 security center, select **Manage ServiceNow configuration** on either of the cards.</span></span> <span data-ttu-id="d6223-151">À partir de là, vous pouvez supprimer la connexion ServiceNow actuelle et personnaliser les noms d’état des tickets.</span><span class="sxs-lookup"><span data-stu-id="d6223-151">From there you can  remove the current ServiceNow connection and customize ticket state names.</span></span>

<span data-ttu-id="d6223-152">Lorsque les tickets ServiceNow sont visibles dans le centre de sécurité Microsoft 365, vos tâches sont placées dans un endroit où elles peuvent être suivies et traitées parallèlement à vos autres éléments de tableau de bord de sécurité.</span><span class="sxs-lookup"><span data-stu-id="d6223-152">With ServiceNow tickets visible in the Microsoft 365 security center, your tasks will live in a place where they can be tracked and acted upon alongside your other security dashboard items.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="d6223-153">Questions fréquemment posées</span><span class="sxs-lookup"><span data-stu-id="d6223-153">Frequently asked questions</span></span>

### <a name="i-am-receiving-an-error-in-the-first-step-of-the-installation-checklist-oauth-creation"></a><span data-ttu-id="d6223-154">Je reçois une erreur dans la première étape de la liste de vérification de l’installation (création OAuth)</span><span class="sxs-lookup"><span data-stu-id="d6223-154">I am receiving an error in the first step of the installation checklist (OAuth creation)</span></span>

<span data-ttu-id="d6223-155">**Message d’erreur**: l’opération de lecture sur « oauth_entity » de l’étendue « x_mioms_m365ticket » a été refusée en raison de la stratégie d’accès aux étendues de la table</span><span class="sxs-lookup"><span data-stu-id="d6223-155">**Error Message**: Read operation against 'oauth_entity' from scope 'x_mioms_m365ticket' has been refused due to the table's cross-scope access policy</span></span>

<span data-ttu-id="d6223-156">Notre application part du principe que n’importe quel administrateur de l’instance de ServiceNow peut créer et lire des entités OAuth.</span><span class="sxs-lookup"><span data-stu-id="d6223-156">Our app assumes any admin on the ServiceNow instance can create and read OAuth entities.</span></span> <span data-ttu-id="d6223-157">Cette erreur peut être due à une personnalisation sur votre instance de ServiceNow, ce qui limite les personnes autorisées à créer/lire des entités OAuth.</span><span class="sxs-lookup"><span data-stu-id="d6223-157">This error could be caused due to a customization on your instance of ServiceNow, which restricts who can create/read OAuth entities.</span></span> <span data-ttu-id="d6223-158">ServiceNow recommande aux utilisateurs de rester à l’extérieur des fonctionnalités (par défaut).</span><span class="sxs-lookup"><span data-stu-id="d6223-158">ServiceNow recommends users keep out of the box functionality (default).</span></span>

<span data-ttu-id="d6223-159">Définissez les configurations des tables « registres des applications » sur par défaut :</span><span class="sxs-lookup"><span data-stu-id="d6223-159">Set the “application registries” table configurations to default:</span></span>

* <span data-ttu-id="d6223-160">Label = registres de l’application</span><span class="sxs-lookup"><span data-stu-id="d6223-160">Label = Application Registeries</span></span>
* <span data-ttu-id="d6223-161">Nom = oauth_entity</span><span class="sxs-lookup"><span data-stu-id="d6223-161">Name = oauth_entity</span></span>
* <span data-ttu-id="d6223-162">Accessible à partir de = toutes les étendues d’application</span><span class="sxs-lookup"><span data-stu-id="d6223-162">Accessible from = All application scopes</span></span>
* <span data-ttu-id="d6223-163">Lecture possible = case à cocher activée</span><span class="sxs-lookup"><span data-stu-id="d6223-163">Can read = check box selected</span></span>

<span data-ttu-id="d6223-164">**ServiceNow recommande aux utilisateurs de rester à l’extérieur des fonctionnalités (par défaut).**</span><span class="sxs-lookup"><span data-stu-id="d6223-164">**ServiceNow recommends users keep out of the box functionality (default).**</span></span>

### <a name="how-do-i-validate-the-oauth-entity-created-for-microsoft-365-security--compliance-connector"></a><span data-ttu-id="d6223-165">Comment puis-je valider l’entité OAuth créée pour Microsoft 365 Security & Compliance Connector ?</span><span class="sxs-lookup"><span data-stu-id="d6223-165">How do I validate the OAuth entity created for Microsoft 365 Security & Compliance connector?</span></span>

<span data-ttu-id="d6223-166">Accédez à la table des registres des applications (menu > système OAuth > application Registry) dans ServiceNow et recherchez l’entité OAuth créée par vous (nom que vous lui avez attribué).</span><span class="sxs-lookup"><span data-stu-id="d6223-166">Go to application registries table (Menu > System OAuth > Application Registry) in ServiceNow and find the OAuth entity created by you (name that you assigned it).</span></span>

### <a name="how-do-i-validate-the-integration-user-created-in-step-two-of-installation-checklist-for-microsoft-365-security--compliance-connector"></a><span data-ttu-id="d6223-167">Comment puis-je valider l’utilisateur d’intégration créé lors de l’étape 2 de la liste de vérification de l’installation pour Microsoft 365 Security & Compliance Connector ?</span><span class="sxs-lookup"><span data-stu-id="d6223-167">How do I validate the Integration User created in step two of installation checklist for Microsoft 365 Security & Compliance connector?</span></span>

<span data-ttu-id="d6223-168">Accédez à la table utilisateurs (menu > l’administration des utilisateurs > les utilisateurs) dans ServiceNow et recherchez l’utilisateur d’intégration que vous avez créé (nom que vous lui avez attribué).</span><span class="sxs-lookup"><span data-stu-id="d6223-168">Go to Users Table (Menu > User Administration > Users) in ServiceNow and find the Integration user created by you (name that you assigned it).</span></span>

<span data-ttu-id="d6223-169">Lors de l’autorisation de la connexion entre le centre de sécurité Microsoft 365 et ServiceNow, veillez à utiliser la connexion utilisateur et le mot de passe d’intégration que vous avez créés lors de la procédure d’installation et pas vos informations d’identification personnelles.</span><span class="sxs-lookup"><span data-stu-id="d6223-169">When authorizing the connection between Microsoft 365 security center and ServiceNow, make sure you use the integration user login and password you created in the installation steps and not your personal credentials.</span></span>

### <a name="i-have-completed-the-installation-and-set-up-steps-but-i-am-unable-to-see-the-servicenow-cards-on-the-home-page-and-cannot-see-the-share-icon-in-microsoft-secure-score"></a><span data-ttu-id="d6223-170">J’ai terminé l’installation et configuré les étapes, mais je ne parviens pas à voir les cartes ServiceNow sur la page d’accueil et je ne vois pas l’icône de partage dans le score de sécurité Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d6223-170">I have completed the installation and set up steps, but I am unable to see the ServiceNow cards on the home page and cannot see the Share icon in Microsoft Secure Score</span></span>

<span data-ttu-id="d6223-171">Vérifiez l’état de la page de mise en service en accédant à https://security.microsoft.com/ticketProvisioning.</span><span class="sxs-lookup"><span data-stu-id="d6223-171">Check the status of the provisioning page by going to https://security.microsoft.com/ticketProvisioning.</span></span> <span data-ttu-id="d6223-172">Sélectionnez **Enregistrer** et revenir à la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="d6223-172">Select **Save** and return to the home page.</span></span> <span data-ttu-id="d6223-173">Les cartes doivent apparaître.</span><span class="sxs-lookup"><span data-stu-id="d6223-173">The cards should appear.</span></span>
