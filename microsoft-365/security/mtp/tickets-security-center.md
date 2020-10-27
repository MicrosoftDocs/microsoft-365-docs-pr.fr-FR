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
ms.openlocfilehash: 8992efdd79295b6b56b8f033bd97b10f59a7a4d5
ms.sourcegitcommit: bd36c88e731e3fee2a3a5cb3564fdc94f11bab94
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2020
ms.locfileid: "48769674"
---
# <a name="create-and-track-servicenow-tickets-in-the-microsoft-365-security-center"></a><span data-ttu-id="821c2-104">Créer et suivre des tickets ServiceNow dans le centre de sécurité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="821c2-104">Create and track ServiceNow tickets in the Microsoft 365 security center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

>[!CAUTION]
><span data-ttu-id="821c2-105">**La période d’aperçu du connecteur ServiceNow se termine**</span><span class="sxs-lookup"><span data-stu-id="821c2-105">**The preview period for the ServiceNow connector is ending**</span></span><br>
><span data-ttu-id="821c2-106">Cette fonctionnalité n’est plus disponible à la fin du 2020 novembre.</span><span class="sxs-lookup"><span data-stu-id="821c2-106">This capability will no longer available by the end of November 2020.</span></span> <span data-ttu-id="821c2-107">Nous vous remercions pour vos commentaires et le support technique pendant que nous déterminons les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="821c2-107">Thank you for your feedback and continued support while we determine next steps.</span></span>

<span data-ttu-id="821c2-108">Le [Centre de sécurité Microsoft 365](overview-security-center.md) a été amélioré grâce à la capacité à créer et suivre en mode natif des tickets dans ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="821c2-108">The [Microsoft 365 security center](overview-security-center.md) has been enhanced with the ability to natively create and track tickets in ServiceNow.</span></span> [<span data-ttu-id="821c2-109">En savoir plus sur ServiceNow</span><span class="sxs-lookup"><span data-stu-id="821c2-109">Learn more about ServiceNow</span></span>](https://www.servicenow.com/)

<span data-ttu-id="821c2-110">Dans le centre de sécurité, les administrateurs de la sécurité peuvent envoyer une action d’amélioration du [score sécurisé Microsoft](microsoft-secure-score.md) directement à ServiceNow et créer un ticket.</span><span class="sxs-lookup"><span data-stu-id="821c2-110">In the security center, security administrators can send a [Microsoft Secure Score](microsoft-secure-score.md) improvement action directly to ServiceNow and create a ticket.</span></span> <span data-ttu-id="821c2-111">Les tickets de gestion des modifications et de gestion des incidents peuvent être créés.</span><span class="sxs-lookup"><span data-stu-id="821c2-111">Both incident management and change management tickets can be created.</span></span> <span data-ttu-id="821c2-112">Suivez les tickets dans la page d’accueil du centre de sécurité et ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="821c2-112">Track tickets in the security center home page and ServiceNow.</span></span>

- [<span data-ttu-id="821c2-113">**En savoir plus sur les conditions préalables, l’échange de données et la résolution des problèmes**</span><span class="sxs-lookup"><span data-stu-id="821c2-113">**Learn about prerequisites, data exchange, and troubleshooting**</span></span>](tickets.md)
- <span data-ttu-id="821c2-114">**Gérer les tickets ServiceNow dans le centre de conformité** (non disponible)</span><span class="sxs-lookup"><span data-stu-id="821c2-114">**Manage ServiceNow tickets in the compliance center** (not available)</span></span>

## <a name="connect-microsoft-365-security-center-to-servicenow"></a><span data-ttu-id="821c2-115">Connecter le centre de sécurité Microsoft 365 à ServiceNow</span><span class="sxs-lookup"><span data-stu-id="821c2-115">Connect Microsoft 365 security center to ServiceNow</span></span>

<span data-ttu-id="821c2-116">Accédez à la page d’accueil du centre de sécurité Microsoft 365 pour afficher la carte de connexion ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="821c2-116">Navigate to the Microsoft 365 security center home page to see the ServiceNow connection card.</span></span>

![Utilisez-vous ServiceNow](../../media/do-you-use-servicenow-250.png)

<span data-ttu-id="821c2-118">Sélectionnez « se connecter à ServiceNow » pour accéder à la page de configuration de ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="821c2-118">Select "Connect to ServiceNow" to go to the ServiceNow setup page.</span></span> <span data-ttu-id="821c2-119">Suivez les instructions pour autoriser l’application Connecteur Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="821c2-119">Follow the instructions to authorize the Microsoft 365 Connector app.</span></span>

> [!NOTE]
> <span data-ttu-id="821c2-120">Avant d’autoriser la connexion entre le centre de sécurité Microsoft 365 et ServiceNow, veillez à utiliser le nom d’utilisateur et le mot de passe d’intégration que vous avez créés lors des étapes d’installation.</span><span class="sxs-lookup"><span data-stu-id="821c2-120">Before you authorize the connection between Microsoft 365 security center and ServiceNow, make sure you use the integration user login and password you created in the installation steps.</span></span> <span data-ttu-id="821c2-121">N’utilisez pas vos informations d’identification personnelles.</span><span class="sxs-lookup"><span data-stu-id="821c2-121">Do not use your personal credentials.</span></span>

<span data-ttu-id="821c2-122">Une fois que vous avez suivi les instructions et autorisé la connexion, affichez l’état de la connexion dans la page de connexion du centre de sécurité Microsoft 365 et dans l’expérience de l’application ServiceNow Microsoft 365 Ticketing Connector.</span><span class="sxs-lookup"><span data-stu-id="821c2-122">After you've followed the directions and authorized the connection, view the connection status in the Microsoft 365 security center connection page and in the ServiceNow Microsoft 365 Ticketing Connector App experience.</span></span> <span data-ttu-id="821c2-123">Vous êtes maintenant prêt à commencer à créer des tâches !</span><span class="sxs-lookup"><span data-stu-id="821c2-123">Now you're all set to start creating tasks!</span></span>

### <a name="troubleshooting"></a><span data-ttu-id="821c2-124">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="821c2-124">Troubleshooting</span></span>

<span data-ttu-id="821c2-125">Découvrez les erreurs courantes que vous pouvez rencontrer dans le processus de connexion et comment les atténuer, dans la [section résolution des problèmes](tickets.md#troubleshooting).</span><span class="sxs-lookup"><span data-stu-id="821c2-125">Learn common errors you may come across in the connection process, and how to mitigate them, in the [troubleshooting section](tickets.md#troubleshooting).</span></span>

## <a name="create-a-task-and-share-it-to-servicenow"></a><span data-ttu-id="821c2-126">Créer une tâche et la partager avec ServiceNow</span><span class="sxs-lookup"><span data-stu-id="821c2-126">Create a task and share it to ServiceNow</span></span>

<span data-ttu-id="821c2-127">Une fois l’intégration configurée, créez des tâches ServiceNow basées sur des actions d’amélioration spécifiques de [Microsoft Secure score](microsoft-secure-score.md) .</span><span class="sxs-lookup"><span data-stu-id="821c2-127">Once the integration is set up, create ServiceNow tasks based on specific [Microsoft Secure Score](microsoft-secure-score.md) improvement actions.</span></span> <span data-ttu-id="821c2-128">Accédez à n’importe quelle action d’amélioration de la note de sécurité dans le centre de sécurité Microsoft 365, puis sélectionnez **partager** .</span><span class="sxs-lookup"><span data-stu-id="821c2-128">Go to any Secure Score improvement action in the Microsoft 365 security center, and select **Share** .</span></span> <span data-ttu-id="821c2-129">L’une des options de liste déroulante est ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="821c2-129">One of the dropdown options is ServiceNow.</span></span>

<span data-ttu-id="821c2-130">Une tâche est générée, dans laquelle vous pouvez définir la priorité et modifier le nom, la description ou la date d’échéance.</span><span class="sxs-lookup"><span data-stu-id="821c2-130">A task is generated where you can set the priority and edit the name, description, or due date.</span></span> <span data-ttu-id="821c2-131">Une fois que tous les champs obligatoires sont renseignés, envoyez la tâche à ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="821c2-131">Once all the required fields are filled in, send the task to ServiceNow.</span></span>

<span data-ttu-id="821c2-132">La tâche est visible dans ServiceNow en tant que demande de modification de la configuration et de la sécurité de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="821c2-132">The task is visible in ServiceNow as a Microsoft 365 Security and Configuration Change Request.</span></span>

## <a name="track-tickets"></a><span data-ttu-id="821c2-133">Suivre les tickets</span><span class="sxs-lookup"><span data-stu-id="821c2-133">Track tickets</span></span>

<span data-ttu-id="821c2-134">Une fois les tickets de gestion des modifications et de gestion des incidents créés, ils sont affichés sur les cartes dans la page d’accueil du centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="821c2-134">Once ServiceNow change management and incident management tickets have been created, they're displayed on cards in the Microsoft 365 security center home page.</span></span> <span data-ttu-id="821c2-135">À partir de ces cartes, vous pouvez créer un ticket, afficher tous les tickets ou gérer la configuration de ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="821c2-135">From these cards, you can create a ticket, view all tickets, or manage the ServiceNow configuration.</span></span>

![Tickets de gestion des modifications ServiceNow](../../media/change-management-375.png)  ![Tickets de gestion des incidents ServiceNow](../../media/incident-management-375.png)

<span data-ttu-id="821c2-138">Pour réapprovisionner ou gérer votre intégration ServiceNow dans le centre de sécurité Microsoft 365, sélectionnez **gérer la configuration de ServiceNow** sur l’une des cartes.</span><span class="sxs-lookup"><span data-stu-id="821c2-138">To reprovision or manage your ServiceNow integration in the Microsoft 365 security center, select **Manage ServiceNow configuration** on either of the cards.</span></span> <span data-ttu-id="821c2-139">À partir de là, supprimez la connexion ServiceNow actuelle et personnalisez les noms d’état des tickets.</span><span class="sxs-lookup"><span data-stu-id="821c2-139">From there, remove the current ServiceNow connection and customize ticket state names.</span></span>

<span data-ttu-id="821c2-140">Avec les tickets ServiceNow visibles dans le centre de sécurité Microsoft 365, vos tâches vivent à un endroit où elles peuvent être suivies et traitées parallèlement à vos autres éléments de tableau de bord de sécurité.</span><span class="sxs-lookup"><span data-stu-id="821c2-140">With ServiceNow tickets visible in the Microsoft 365 security center, your tasks live in a place where they can be tracked and acted upon alongside your other security dashboard items.</span></span>

## <a name="resources"></a><span data-ttu-id="821c2-141">Ressources</span><span class="sxs-lookup"><span data-stu-id="821c2-141">Resources</span></span>

- [<span data-ttu-id="821c2-142">En savoir plus sur les conditions préalables, l’échange de données et la résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="821c2-142">Learn about prerequisites, data exchange, and troubleshooting</span></span>](tickets.md)
- [<span data-ttu-id="821c2-143">Niveau de sécurité Microsoft</span><span class="sxs-lookup"><span data-stu-id="821c2-143">Microsoft Secure Score</span></span>](microsoft-secure-score.md)
