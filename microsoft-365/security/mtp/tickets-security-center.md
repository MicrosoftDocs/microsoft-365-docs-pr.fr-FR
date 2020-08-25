---
title: Créer et suivre des tickets ServiceNow dans le centre de sécurité Microsoft 365
description: Découvrez comment créer et suivre des tickets dans ServiceNow à partir du centre de sécurité Microsoft 365.
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
ms.custom:
- seo-marvel-apr2020
ms.openlocfilehash: bd5bf8533d38337c063acdf0dda073e4961e416a
ms.sourcegitcommit: 787b198765565d54ee73972f664bdbd5023d666b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/24/2020
ms.locfileid: "46867244"
---
# <a name="create-and-track-servicenow-tickets-in-the-microsoft-365-security-center"></a><span data-ttu-id="30c72-104">Créer et suivre des tickets ServiceNow dans le centre de sécurité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="30c72-104">Create and track ServiceNow tickets in the Microsoft 365 security center</span></span>

<span data-ttu-id="30c72-105">Le [Centre de sécurité Microsoft 365](overview-security-center.md) a été amélioré grâce à la capacité à créer et suivre en mode natif des tickets dans ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="30c72-105">The [Microsoft 365 security center](overview-security-center.md) has been enhanced with the ability to natively create and track tickets in ServiceNow.</span></span> [<span data-ttu-id="30c72-106">En savoir plus sur ServiceNow</span><span class="sxs-lookup"><span data-stu-id="30c72-106">Learn more about ServiceNow</span></span>](https://www.servicenow.com/)

<span data-ttu-id="30c72-107">Dans le centre de sécurité, les administrateurs de la sécurité peuvent envoyer une action d’amélioration du [score sécurisé Microsoft](microsoft-secure-score.md) directement à ServiceNow et créer un ticket.</span><span class="sxs-lookup"><span data-stu-id="30c72-107">In the security center, security administrators can send a [Microsoft Secure Score](microsoft-secure-score.md) improvement action directly to ServiceNow and create a ticket.</span></span> <span data-ttu-id="30c72-108">Les tickets de gestion des modifications et de gestion des incidents peuvent être créés.</span><span class="sxs-lookup"><span data-stu-id="30c72-108">Both incident management and change management tickets can be created.</span></span> <span data-ttu-id="30c72-109">Suivez les tickets dans la page d’accueil du centre de sécurité et ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="30c72-109">Track tickets in the security center home page and ServiceNow.</span></span>

- [<span data-ttu-id="30c72-110">**En savoir plus sur les conditions préalables, l’échange de données et la résolution des problèmes**</span><span class="sxs-lookup"><span data-stu-id="30c72-110">**Learn about prerequisites, data exchange, and troubleshooting**</span></span>](tickets.md)
- <span data-ttu-id="30c72-111">**Gérer les tickets ServiceNow dans le centre de conformité** (bientôt disponible)</span><span class="sxs-lookup"><span data-stu-id="30c72-111">**Manage ServiceNow tickets in the compliance center** (coming soon)</span></span>

## <a name="connect-microsoft-365-security-center-to-servicenow"></a><span data-ttu-id="30c72-112">Connecter le centre de sécurité Microsoft 365 à ServiceNow</span><span class="sxs-lookup"><span data-stu-id="30c72-112">Connect Microsoft 365 security center to ServiceNow</span></span>

<span data-ttu-id="30c72-113">Accédez à la page d’accueil du centre de sécurité Microsoft 365 pour afficher la carte de connexion ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="30c72-113">Navigate to the Microsoft 365 security center home page to see the ServiceNow connection card.</span></span>

![Utilisez-vous ServiceNow](../../media/do-you-use-servicenow-250.png)

<span data-ttu-id="30c72-115">Sélectionnez « se connecter à ServiceNow » pour accéder à la page de configuration de ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="30c72-115">Select "Connect to ServiceNow" to go to the ServiceNow setup page.</span></span> <span data-ttu-id="30c72-116">Suivez les instructions pour autoriser l’application Connecteur Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="30c72-116">Follow the instructions to authorize the Microsoft 365 Connector app.</span></span>

> [!NOTE]
> <span data-ttu-id="30c72-117">Avant d’autoriser la connexion entre le centre de sécurité Microsoft 365 et ServiceNow, veillez à utiliser le nom d’utilisateur et le mot de passe d’intégration que vous avez créés lors des étapes d’installation.</span><span class="sxs-lookup"><span data-stu-id="30c72-117">Before you authorize the connection between Microsoft 365 security center and ServiceNow, make sure you use the integration user login and password you created in the installation steps.</span></span> <span data-ttu-id="30c72-118">N’utilisez pas vos informations d’identification personnelles.</span><span class="sxs-lookup"><span data-stu-id="30c72-118">Do not use your personal credentials.</span></span>

<span data-ttu-id="30c72-119">Une fois que vous avez suivi les instructions et autorisé la connexion, affichez l’état de la connexion dans la page de connexion du centre de sécurité Microsoft 365 et dans l’expérience de l’application ServiceNow Microsoft 365 Ticketing Connector.</span><span class="sxs-lookup"><span data-stu-id="30c72-119">After you've followed the directions and authorized the connection, view the connection status in the Microsoft 365 security center connection page and in the ServiceNow Microsoft 365 Ticketing Connector App experience.</span></span> <span data-ttu-id="30c72-120">Vous êtes maintenant prêt à commencer à créer des tâches !</span><span class="sxs-lookup"><span data-stu-id="30c72-120">Now you're all set to start creating tasks!</span></span>

### <a name="troubleshooting"></a><span data-ttu-id="30c72-121">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="30c72-121">Troubleshooting</span></span>

<span data-ttu-id="30c72-122">Découvrez les erreurs courantes que vous pouvez rencontrer dans le processus de connexion et comment les atténuer, dans la [section résolution des problèmes](tickets.md#troubleshooting).</span><span class="sxs-lookup"><span data-stu-id="30c72-122">Learn common errors you may come across in the connection process, and how to mitigate them, in the [troubleshooting section](tickets.md#troubleshooting).</span></span>

## <a name="create-a-task-and-share-it-to-servicenow"></a><span data-ttu-id="30c72-123">Créer une tâche et la partager avec ServiceNow</span><span class="sxs-lookup"><span data-stu-id="30c72-123">Create a task and share it to ServiceNow</span></span>

<span data-ttu-id="30c72-124">Une fois l’intégration configurée, créez des tâches ServiceNow basées sur des actions d’amélioration spécifiques de [Microsoft Secure score](microsoft-secure-score.md) .</span><span class="sxs-lookup"><span data-stu-id="30c72-124">Once the integration is set up, create ServiceNow tasks based on specific [Microsoft Secure Score](microsoft-secure-score.md) improvement actions.</span></span> <span data-ttu-id="30c72-125">Accédez à n’importe quelle action d’amélioration de la note de sécurité dans le centre de sécurité Microsoft 365, puis sélectionnez **partager**.</span><span class="sxs-lookup"><span data-stu-id="30c72-125">Go to any Secure Score improvement action in the Microsoft 365 security center, and select **Share**.</span></span> <span data-ttu-id="30c72-126">L’une des options de liste déroulante est ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="30c72-126">One of the dropdown options is ServiceNow.</span></span>

<span data-ttu-id="30c72-127">Une tâche est générée, dans laquelle vous pouvez définir la priorité et modifier le nom, la description ou la date d’échéance.</span><span class="sxs-lookup"><span data-stu-id="30c72-127">A task is generated where you can set the priority and edit the name, description, or due date.</span></span> <span data-ttu-id="30c72-128">Une fois que tous les champs obligatoires sont renseignés, envoyez la tâche à ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="30c72-128">Once all the required fields are filled in, send the task to ServiceNow.</span></span>

<span data-ttu-id="30c72-129">La tâche est visible dans ServiceNow en tant que demande de modification de la configuration et de la sécurité de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="30c72-129">The task is visible in ServiceNow as a Microsoft 365 Security and Configuration Change Request.</span></span>

## <a name="track-tickets"></a><span data-ttu-id="30c72-130">Suivre les tickets</span><span class="sxs-lookup"><span data-stu-id="30c72-130">Track tickets</span></span>

<span data-ttu-id="30c72-131">Une fois les tickets de gestion des modifications et de gestion des incidents créés, ils sont affichés sur les cartes dans la page d’accueil du centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="30c72-131">Once ServiceNow change management and incident management tickets have been created, they're displayed on cards in the Microsoft 365 security center home page.</span></span> <span data-ttu-id="30c72-132">À partir de ces cartes, vous pouvez créer un ticket, afficher tous les tickets ou gérer la configuration de ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="30c72-132">From these cards, you can create a ticket, view all tickets, or manage the ServiceNow configuration.</span></span>

![Tickets de gestion des modifications ServiceNow](../../media/change-management-375.png)  ![Tickets de gestion des incidents ServiceNow](../../media/incident-management-375.png)

<span data-ttu-id="30c72-135">Pour réapprovisionner ou gérer votre intégration ServiceNow dans le centre de sécurité Microsoft 365, sélectionnez **gérer la configuration de ServiceNow** sur l’une des cartes.</span><span class="sxs-lookup"><span data-stu-id="30c72-135">To reprovision or manage your ServiceNow integration in the Microsoft 365 security center, select **Manage ServiceNow configuration** on either of the cards.</span></span> <span data-ttu-id="30c72-136">À partir de là, supprimez la connexion ServiceNow actuelle et personnalisez les noms d’état des tickets.</span><span class="sxs-lookup"><span data-stu-id="30c72-136">From there, remove the current ServiceNow connection and customize ticket state names.</span></span>

<span data-ttu-id="30c72-137">Avec les tickets ServiceNow visibles dans le centre de sécurité Microsoft 365, vos tâches vivent à un endroit où elles peuvent être suivies et traitées parallèlement à vos autres éléments de tableau de bord de sécurité.</span><span class="sxs-lookup"><span data-stu-id="30c72-137">With ServiceNow tickets visible in the Microsoft 365 security center, your tasks live in a place where they can be tracked and acted upon alongside your other security dashboard items.</span></span>

## <a name="resources"></a><span data-ttu-id="30c72-138">Ressources</span><span class="sxs-lookup"><span data-stu-id="30c72-138">Resources</span></span>

- [<span data-ttu-id="30c72-139">En savoir plus sur les conditions préalables, l’échange de données et la résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="30c72-139">Learn about prerequisites, data exchange, and troubleshooting</span></span>](tickets.md)
- [<span data-ttu-id="30c72-140">Niveau de sécurité Microsoft</span><span class="sxs-lookup"><span data-stu-id="30c72-140">Microsoft Secure Score</span></span>](microsoft-secure-score.md)