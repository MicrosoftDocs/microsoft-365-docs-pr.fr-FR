---
title: Examiner un compte d’utilisateur dans Microsoft Defender ATP
description: Examiner un compte d’utilisateur à la recherche d’informations d’identification potentiellement compromises ou pivoter sur le compte d’utilisateur associé au cours d’une enquête.
keywords: examiner, compte, utilisateur, entité utilisateur, alerte, microsoft defender atp
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: article
ms.date: 04/24/2018
ms.technology: mde
ms.openlocfilehash: e994069220d8f88f1b8910413ad86da399c4a8f3
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51064294"
---
# <a name="investigate-a-user-account-in-microsoft-defender-for-endpoint"></a><span data-ttu-id="7b9c6-104">Examiner un compte d’utilisateur dans Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="7b9c6-104">Investigate a user account in Microsoft Defender for Endpoint</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="7b9c6-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="7b9c6-105">**Applies to:**</span></span>
- [<span data-ttu-id="7b9c6-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="7b9c6-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2146631)
- [<span data-ttu-id="7b9c6-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="7b9c6-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


><span data-ttu-id="7b9c6-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="7b9c6-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="7b9c6-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="7b9c6-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigatgeuser-abovefoldlink)

## <a name="investigate-user-account-entities"></a><span data-ttu-id="7b9c6-110">Examiner les entités de compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="7b9c6-110">Investigate user account entities</span></span>

<span data-ttu-id="7b9c6-111">Identifiez les comptes d’utilisateurs avec les alertes les plus actives (affichées sur le tableau de bord sous la forme « Utilisateurs à risque ») et examinez les cas d’informations d’identification potentiellement compromises, ou faites pivoter le compte d’utilisateur associé lors de l’examen d’une alerte ou d’un appareil afin d’identifier les éventuels mouvements latérals entre les appareils avec ce compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7b9c6-111">Identify user accounts with the most active alerts (displayed on dashboard as "Users at risk") and investigate cases of potential compromised credentials, or pivot on the associated user account when investigating an alert or device to identify possible lateral movement between devices with that user account.</span></span>

<span data-ttu-id="7b9c6-112">Les informations de compte d’utilisateur sont disponibles dans les affichages suivants :</span><span class="sxs-lookup"><span data-stu-id="7b9c6-112">You can find user account information in the following views:</span></span>

- <span data-ttu-id="7b9c6-113">Tableau de bord</span><span class="sxs-lookup"><span data-stu-id="7b9c6-113">Dashboard</span></span>
- <span data-ttu-id="7b9c6-114">File d’attente des alertes</span><span class="sxs-lookup"><span data-stu-id="7b9c6-114">Alert queue</span></span>
- <span data-ttu-id="7b9c6-115">Page Détails de l’appareil</span><span class="sxs-lookup"><span data-stu-id="7b9c6-115">Device details page</span></span>

<span data-ttu-id="7b9c6-116">Un lien de compte d’utilisateur cliquable est disponible dans ces affichages, qui vous permet d’obtenir la page de détails du compte d’utilisateur dans laquelle des détails plus détaillés sur le compte d’utilisateur sont affichés.</span><span class="sxs-lookup"><span data-stu-id="7b9c6-116">A clickable user account link is available in these views, that will take you to the user account details page where more details about the user account are shown.</span></span>

<span data-ttu-id="7b9c6-117">Lorsque vous examinez une entité de compte d’utilisateur, vous voyez :</span><span class="sxs-lookup"><span data-stu-id="7b9c6-117">When you investigate a user account entity, you'll see:</span></span>

- <span data-ttu-id="7b9c6-118">Détails du compte d’utilisateur, alertes Azure Advanced Threat Protection (Azure ATP) et appareils connectés, rôle, type de session et autres détails</span><span class="sxs-lookup"><span data-stu-id="7b9c6-118">User account details, Azure Advanced Threat Protection (Azure ATP) alerts, and logged on devices, role, logon type, and other details</span></span>
- <span data-ttu-id="7b9c6-119">Vue d’ensemble des incidents et des appareils de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="7b9c6-119">Overview of the incidents and user's devices</span></span>
- <span data-ttu-id="7b9c6-120">Alertes associées à cet utilisateur</span><span class="sxs-lookup"><span data-stu-id="7b9c6-120">Alerts related to this user</span></span>
- <span data-ttu-id="7b9c6-121">Observé dans l’organisation (appareils connectés)</span><span class="sxs-lookup"><span data-stu-id="7b9c6-121">Observed in organization (devices logged on to)</span></span>

![Image de la page de détails de l’entité du compte d’utilisateur](images/atp-user-details-view.png)

### <a name="user-details"></a><span data-ttu-id="7b9c6-123">Détails de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="7b9c6-123">User details</span></span>

<span data-ttu-id="7b9c6-124">Le  volet d’informations utilisateur de gauche fournit des informations sur l’utilisateur, telles que les incidents d’ouverture connexes, les alertes actives, le nom SAM, le SID, les alertes Azure ATP, le nombre d’appareils avec qui l’utilisateur est connecté, la première fois que l’utilisateur a été vu pour la première fois, le rôle et les types d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="7b9c6-124">The **User details** pane on left provides information about the user, such as related open incidents, active alerts, SAM name, SID, Azure ATP alerts, number of devices the user is logged on to, when the user was first and last seen, role, and logon types.</span></span> <span data-ttu-id="7b9c6-125">Selon les fonctionnalités d’intégration que vous avez activées, vous verrez d’autres détails.</span><span class="sxs-lookup"><span data-stu-id="7b9c6-125">Depending on the integration features you've enabled, you'll see other details.</span></span> <span data-ttu-id="7b9c6-126">Par exemple, si vous activez l’intégration de Skype Entreprise, vous pourrez contacter l’utilisateur à partir du portail.</span><span class="sxs-lookup"><span data-stu-id="7b9c6-126">For example, if you enable the Skype for business integration, you'll be able to contact the user from the portal.</span></span> <span data-ttu-id="7b9c6-127">La section **Alertes Azure ATP** contient un lien qui vous permet d’accès à la page Azure ATP, si vous avez activé la fonctionnalité Azure ATP et qu’il existe des alertes relatives à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7b9c6-127">The **Azure ATP alerts** section contains a link that will take you to the Azure ATP page, if you have enabled the Azure ATP feature, and there are alerts related to the user.</span></span> <span data-ttu-id="7b9c6-128">La page Azure ATP fournit plus d’informations sur les alertes.</span><span class="sxs-lookup"><span data-stu-id="7b9c6-128">The Azure ATP page will provide more information about the alerts.</span></span>

>[!NOTE]
><span data-ttu-id="7b9c6-129">Vous devez activer l’intégration sur Azure ATP et Defender for Endpoint pour utiliser cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="7b9c6-129">You'll need to enable the integration on both Azure ATP and Defender for Endpoint to use this feature.</span></span> <span data-ttu-id="7b9c6-130">Dans Defender pour point de terminaison, vous pouvez activer cette fonctionnalité dans les fonctionnalités avancées.</span><span class="sxs-lookup"><span data-stu-id="7b9c6-130">In Defender for Endpoint, you can enable this feature in advanced features.</span></span> <span data-ttu-id="7b9c6-131">Pour plus d’informations sur l’activer, voir [Activer les fonctionnalités avancées.](advanced-features.md)</span><span class="sxs-lookup"><span data-stu-id="7b9c6-131">For more information on how to enable advanced features, see [Turn on advanced features](advanced-features.md).</span></span>

<span data-ttu-id="7b9c6-132">La vue d’ensemble, les alertes et les observations dans l’organisation sont des onglets différents qui affichent différents attributs sur le compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7b9c6-132">The Overview, Alerts, and Observed in organization are different tabs that display various attributes about the user account.</span></span>

### <a name="overview"></a><span data-ttu-id="7b9c6-133">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="7b9c6-133">Overview</span></span>

<span data-ttu-id="7b9c6-134">**L’onglet** Vue d’ensemble affiche les détails des incidents et une liste des appareils sur qui l’utilisateur s’est connecté.</span><span class="sxs-lookup"><span data-stu-id="7b9c6-134">The **Overview** tab shows the incidents details and a list of the devices that the user has logged on to.</span></span> <span data-ttu-id="7b9c6-135">Vous pouvez les développer pour voir les détails des événements de connexion pour chaque appareil.</span><span class="sxs-lookup"><span data-stu-id="7b9c6-135">You can expand these to see details of the log-on events for each device.</span></span>

### <a name="alerts"></a><span data-ttu-id="7b9c6-136">Alertes</span><span class="sxs-lookup"><span data-stu-id="7b9c6-136">Alerts</span></span>

<span data-ttu-id="7b9c6-137">**L’onglet Alertes** fournit une liste des alertes associées au compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7b9c6-137">The **Alerts** tab provides a list of alerts that are associated with the user account.</span></span> <span data-ttu-id="7b9c6-138">Cette liste est une vue [](alerts-queue.md)filtrée de la file d’attente des alertes et affiche les alertes où le contexte utilisateur est le compte d’utilisateur sélectionné, la date à laquelle la dernière activité a été détectée, une brève description de l’alerte, le périphérique associé à l’alerte, la gravité de l’alerte, l’état de l’alerte dans la file d’attente et l’utilisateur affecté à l’alerte.</span><span class="sxs-lookup"><span data-stu-id="7b9c6-138">This list is a filtered view of the [Alert queue](alerts-queue.md), and shows alerts where the user context is the selected user account, the date when the last activity was detected, a short description of the alert, the device associated with the alert, the alert's severity, the alert's status in the queue, and who is assigned the alert.</span></span>

### <a name="observed-in-organization"></a><span data-ttu-id="7b9c6-139">Observé dans l’organisation</span><span class="sxs-lookup"><span data-stu-id="7b9c6-139">Observed in organization</span></span>

<span data-ttu-id="7b9c6-140">L’onglet Observé dans l’organisation vous permet de spécifier une plage de dates pour voir la liste des appareils sur lequel cet utilisateur a été connecté, le compte d’utilisateur connecté le plus fréquent et le moins fréquent pour chacun de ces appareils et le nombre total d’utilisateurs observés sur chaque appareil. </span><span class="sxs-lookup"><span data-stu-id="7b9c6-140">The **Observed in organization** tab allows you to specify a date range to see a list of devices where this user was observed logged on to, the most frequent and least frequent logged on user account for each of these devices, and total observed users on each device.</span></span>

<span data-ttu-id="7b9c6-141">La sélection d’un élément dans le tableau Observé dans l’organisation développera l’élément, révélant plus de détails sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7b9c6-141">Selecting an item on the Observed in organization table will expand the item, revealing more details about the device.</span></span> <span data-ttu-id="7b9c6-142">La sélection directe d’un lien au sein d’un élément vous enverra à la page correspondante.</span><span class="sxs-lookup"><span data-stu-id="7b9c6-142">Directly selecting a link within an item will send you to the corresponding page.</span></span>

## <a name="search-for-specific-user-accounts"></a><span data-ttu-id="7b9c6-143">Rechercher des comptes d’utilisateurs spécifiques</span><span class="sxs-lookup"><span data-stu-id="7b9c6-143">Search for specific user accounts</span></span>

1. <span data-ttu-id="7b9c6-144">Sélectionnez **Utilisateur** dans le menu déroulant **de la** barre de recherche.</span><span class="sxs-lookup"><span data-stu-id="7b9c6-144">Select **User** from the **Search bar** drop-down menu.</span></span>
2. <span data-ttu-id="7b9c6-145">Entrez le compte d’utilisateur dans le **champ** Recherche.</span><span class="sxs-lookup"><span data-stu-id="7b9c6-145">Enter the user account in the **Search** field.</span></span>
3. <span data-ttu-id="7b9c6-146">Cliquez sur l’icône de recherche ou appuyez sur **Entrée.**</span><span class="sxs-lookup"><span data-stu-id="7b9c6-146">Click the search icon or press **Enter**.</span></span>

<span data-ttu-id="7b9c6-147">Une liste d’utilisateurs correspondant au texte de la requête s’affiche.</span><span class="sxs-lookup"><span data-stu-id="7b9c6-147">A list of users matching the query text is displayed.</span></span> <span data-ttu-id="7b9c6-148">Vous verrez le domaine et le nom du compte d’utilisateur, la dernière fois que le compte d’utilisateur a été vu, ainsi que le nombre total d’appareils sur qui il a été connecté au cours des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="7b9c6-148">You'll see the user account's domain and name, when the user account was last seen, and the total number of devices it was observed logged on to in the last 30 days.</span></span>

<span data-ttu-id="7b9c6-149">Vous pouvez filtrer les résultats selon les périodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="7b9c6-149">You can filter the results by the following time periods:</span></span>

- <span data-ttu-id="7b9c6-150">1 jour</span><span class="sxs-lookup"><span data-stu-id="7b9c6-150">1 day</span></span>
- <span data-ttu-id="7b9c6-151">3 jours</span><span class="sxs-lookup"><span data-stu-id="7b9c6-151">3 days</span></span>
- <span data-ttu-id="7b9c6-152">7 jours</span><span class="sxs-lookup"><span data-stu-id="7b9c6-152">7 days</span></span>
- <span data-ttu-id="7b9c6-153">30 jours</span><span class="sxs-lookup"><span data-stu-id="7b9c6-153">30 days</span></span>
- <span data-ttu-id="7b9c6-154">6 mois</span><span class="sxs-lookup"><span data-stu-id="7b9c6-154">6 months</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b9c6-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b9c6-155">Related topics</span></span>

- [<span data-ttu-id="7b9c6-156">Afficher et organiser la file d’attente des alertes microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="7b9c6-156">View and organize the Microsoft Defender for Endpoint Alerts queue</span></span>](alerts-queue.md)
- [<span data-ttu-id="7b9c6-157">Gérer les alertes microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="7b9c6-157">Manage Microsoft Defender for Endpoint alerts</span></span>](manage-alerts.md)
- [<span data-ttu-id="7b9c6-158">Examiner microsoft Defender pour les alertes de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="7b9c6-158">Investigate Microsoft Defender for Endpoint alerts</span></span>](investigate-alerts.md)
- [<span data-ttu-id="7b9c6-159">Examiner un fichier associé à une alerte Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="7b9c6-159">Investigate a file associated with a Defender for Endpoint alert</span></span>](investigate-files.md)
- [<span data-ttu-id="7b9c6-160">Examiner les appareils dans la liste Defender pour les appareils de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="7b9c6-160">Investigate devices in the Defender for Endpoint Devices list</span></span>](investigate-machines.md)
- [<span data-ttu-id="7b9c6-161">Examiner une adresse IP associée à une alerte Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="7b9c6-161">Investigate an IP address associated with a Defender for Endpoint alert</span></span>](investigate-ip.md)
- [<span data-ttu-id="7b9c6-162">Examiner un domaine associé à une alerte Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="7b9c6-162">Investigate a domain associated with a Defender for Endpoint alert</span></span>](investigate-domain.md)
