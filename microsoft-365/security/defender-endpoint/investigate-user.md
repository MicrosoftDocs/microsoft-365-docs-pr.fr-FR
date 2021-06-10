---
title: Examiner un compte d’utilisateur dans Microsoft Defender pour le point de terminaison
description: Examiner un compte d’utilisateur à la recherche d’informations d’identification compromises ou pivoter sur le compte d’utilisateur associé au cours d’une enquête.
keywords: examiner, compte, utilisateur, entité utilisateur, alerte, Microsoft Defender pour le point de terminaison
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
ms.openlocfilehash: e98142e4076c5e695f16eb06c062bc69d3d7dd55
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51935064"
---
# <a name="investigate-a-user-account-in-microsoft-defender-for-endpoint"></a><span data-ttu-id="9250b-104">Examiner un compte d’utilisateur dans Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="9250b-104">Investigate a user account in Microsoft Defender for Endpoint</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="9250b-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="9250b-105">**Applies to:**</span></span>
- [<span data-ttu-id="9250b-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="9250b-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="9250b-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="9250b-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


><span data-ttu-id="9250b-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="9250b-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="9250b-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="9250b-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigatgeuser-abovefoldlink)

## <a name="investigate-user-account-entities"></a><span data-ttu-id="9250b-110">Examiner les entités de compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="9250b-110">Investigate user account entities</span></span>

<span data-ttu-id="9250b-111">Identifiez les comptes d’utilisateurs avec les alertes les plus actives (affichées sur le tableau de bord sous la forme « Utilisateurs à risque ») et examinez les cas d’informations d’identification potentiellement compromises, ou faites pivoter le compte d’utilisateur associé lors de l’examen d’une alerte ou d’un appareil afin d’identifier les éventuels mouvements latérals entre les appareils avec ce compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9250b-111">Identify user accounts with the most active alerts (displayed on dashboard as "Users at risk") and investigate cases of potential compromised credentials, or pivot on the associated user account when investigating an alert or device to identify possible lateral movement between devices with that user account.</span></span>

<span data-ttu-id="9250b-112">Les informations de compte d’utilisateur sont disponibles dans les affichages suivants :</span><span class="sxs-lookup"><span data-stu-id="9250b-112">You can find user account information in the following views:</span></span>

- <span data-ttu-id="9250b-113">Tableau de bord</span><span class="sxs-lookup"><span data-stu-id="9250b-113">Dashboard</span></span>
- <span data-ttu-id="9250b-114">File d’attente des alertes</span><span class="sxs-lookup"><span data-stu-id="9250b-114">Alert queue</span></span>
- <span data-ttu-id="9250b-115">Page Détails de l’appareil</span><span class="sxs-lookup"><span data-stu-id="9250b-115">Device details page</span></span>

<span data-ttu-id="9250b-116">Un lien de compte d’utilisateur cliquable est disponible dans ces affichages, qui vous permet d’obtenir la page de détails du compte d’utilisateur dans laquelle des détails plus détaillés sur le compte d’utilisateur sont affichés.</span><span class="sxs-lookup"><span data-stu-id="9250b-116">A clickable user account link is available in these views, that will take you to the user account details page where more details about the user account are shown.</span></span>

<span data-ttu-id="9250b-117">Lorsque vous examinez une entité de compte d’utilisateur, vous voyez :</span><span class="sxs-lookup"><span data-stu-id="9250b-117">When you investigate a user account entity, you'll see:</span></span>

- <span data-ttu-id="9250b-118">Détails du compte d’utilisateur, alertes Microsoft Defender pour l’identité et appareils connectés, rôle, type de session et autres détails</span><span class="sxs-lookup"><span data-stu-id="9250b-118">User account details, Microsoft Defender for Identity alerts, and logged on devices, role, logon type, and other details</span></span>
- <span data-ttu-id="9250b-119">Vue d’ensemble des incidents et des appareils de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="9250b-119">Overview of the incidents and user's devices</span></span>
- <span data-ttu-id="9250b-120">Alertes associées à cet utilisateur</span><span class="sxs-lookup"><span data-stu-id="9250b-120">Alerts related to this user</span></span>
- <span data-ttu-id="9250b-121">Observé dans l’organisation (appareils connectés)</span><span class="sxs-lookup"><span data-stu-id="9250b-121">Observed in organization (devices logged on to)</span></span>

![Image de la page de détails de l’entité du compte d’utilisateur](images/atp-user-details-view.png)

### <a name="user-details"></a><span data-ttu-id="9250b-123">Détails de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="9250b-123">User details</span></span>

<span data-ttu-id="9250b-124">Le  volet d’informations Utilisateur de gauche fournit des informations sur l’utilisateur, telles que les incidents d’ouverture connexes, les alertes actives, le nom SAM, le SID, les alertes Microsoft Defender pour l’identité, le nombre d’appareils avec qui l’utilisateur est connecté, la première fois que l’utilisateur a été vu pour la première fois, le rôle et les types d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="9250b-124">The **User details** pane on left provides information about the user, such as related open incidents, active alerts, SAM name, SID, Microsoft Defender for Identity alerts, number of devices the user is logged on to, when the user was first and last seen, role, and logon types.</span></span> <span data-ttu-id="9250b-125">Selon les fonctionnalités d’intégration que vous avez activées, vous verrez d’autres détails.</span><span class="sxs-lookup"><span data-stu-id="9250b-125">Depending on the integration features you've enabled, you'll see other details.</span></span> <span data-ttu-id="9250b-126">Par exemple, si vous activez l’Skype pour l’intégration d’entreprise, vous pourrez contacter l’utilisateur à partir du portail.</span><span class="sxs-lookup"><span data-stu-id="9250b-126">For example, if you enable the Skype for business integration, you'll be able to contact the user from the portal.</span></span> <span data-ttu-id="9250b-127">La section **Alertes Azure ATP** contient un lien qui vous permet d’accès à la page Microsoft Defender pour l’identité, si vous avez activé la fonctionnalité Microsoft Defender pour l’identité et que des alertes sont associées à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9250b-127">The **Azure ATP alerts** section contains a link that will take you to the Microsoft Defender for Identity page, if you have enabled the Microsoft Defender for Identity feature, and there are alerts related to the user.</span></span> <span data-ttu-id="9250b-128">La page Microsoft Defender pour l’identité fournit plus d’informations sur les alertes.</span><span class="sxs-lookup"><span data-stu-id="9250b-128">The Microsoft Defender for Identity page will provide more information about the alerts.</span></span>

>[!NOTE]
><span data-ttu-id="9250b-129">Vous devez activer l’intégration sur Microsoft Defender pour l’identité et Defender pour le point de terminaison pour utiliser cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="9250b-129">You'll need to enable the integration on both Microsoft Defender for Identity and Defender for Endpoint to use this feature.</span></span> <span data-ttu-id="9250b-130">Dans Defender pour point de terminaison, vous pouvez activer cette fonctionnalité dans les fonctionnalités avancées.</span><span class="sxs-lookup"><span data-stu-id="9250b-130">In Defender for Endpoint, you can enable this feature in advanced features.</span></span> <span data-ttu-id="9250b-131">Pour plus d’informations sur l’activer, voir [Activer les fonctionnalités avancées.](advanced-features.md)</span><span class="sxs-lookup"><span data-stu-id="9250b-131">For more information on how to enable advanced features, see [Turn on advanced features](advanced-features.md).</span></span>

<span data-ttu-id="9250b-132">La vue d’ensemble, les alertes et les observations dans l’organisation sont des onglets différents qui affichent différents attributs sur le compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9250b-132">The Overview, Alerts, and Observed in organization are different tabs that display various attributes about the user account.</span></span>

### <a name="overview"></a><span data-ttu-id="9250b-133">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="9250b-133">Overview</span></span>

<span data-ttu-id="9250b-134">**L’onglet** Vue d’ensemble affiche les détails des incidents et une liste des appareils sur qui l’utilisateur s’est connecté.</span><span class="sxs-lookup"><span data-stu-id="9250b-134">The **Overview** tab shows the incidents details and a list of the devices that the user has logged on to.</span></span> <span data-ttu-id="9250b-135">Vous pouvez les développer pour voir les détails des événements de connexion pour chaque appareil.</span><span class="sxs-lookup"><span data-stu-id="9250b-135">You can expand these to see details of the log-on events for each device.</span></span>

### <a name="alerts"></a><span data-ttu-id="9250b-136">Alertes</span><span class="sxs-lookup"><span data-stu-id="9250b-136">Alerts</span></span>

<span data-ttu-id="9250b-137">**L’onglet Alertes** fournit une liste des alertes associées au compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9250b-137">The **Alerts** tab provides a list of alerts that are associated with the user account.</span></span> <span data-ttu-id="9250b-138">Cette liste est une vue [](alerts-queue.md)filtrée de la file d’attente des alertes et affiche les alertes où le contexte utilisateur est le compte d’utilisateur sélectionné, la date à laquelle la dernière activité a été détectée, une brève description de l’alerte, le périphérique associé à l’alerte, la gravité de l’alerte, l’état de l’alerte dans la file d’attente et l’utilisateur affecté à l’alerte.</span><span class="sxs-lookup"><span data-stu-id="9250b-138">This list is a filtered view of the [Alert queue](alerts-queue.md), and shows alerts where the user context is the selected user account, the date when the last activity was detected, a short description of the alert, the device associated with the alert, the alert's severity, the alert's status in the queue, and who is assigned the alert.</span></span>

### <a name="observed-in-organization"></a><span data-ttu-id="9250b-139">Observé dans l’organisation</span><span class="sxs-lookup"><span data-stu-id="9250b-139">Observed in organization</span></span>

<span data-ttu-id="9250b-140">L’onglet Observé dans l’organisation vous permet de spécifier une plage de dates pour voir la liste des appareils sur lequel cet utilisateur a été connecté, le compte d’utilisateur connecté le plus fréquent et le moins fréquent pour chacun de ces appareils et le nombre total d’utilisateurs observés sur chaque appareil. </span><span class="sxs-lookup"><span data-stu-id="9250b-140">The **Observed in organization** tab allows you to specify a date range to see a list of devices where this user was observed logged on to, the most frequent and least frequent logged on user account for each of these devices, and total observed users on each device.</span></span>

<span data-ttu-id="9250b-141">La sélection d’un élément dans le tableau Observé dans l’organisation développera l’élément, révélant plus de détails sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9250b-141">Selecting an item on the Observed in organization table will expand the item, revealing more details about the device.</span></span> <span data-ttu-id="9250b-142">La sélection directe d’un lien dans un élément vous enverra à la page correspondante.</span><span class="sxs-lookup"><span data-stu-id="9250b-142">Directly selecting a link within an item will send you to the corresponding page.</span></span>

## <a name="search-for-specific-user-accounts"></a><span data-ttu-id="9250b-143">Rechercher des comptes d’utilisateurs spécifiques</span><span class="sxs-lookup"><span data-stu-id="9250b-143">Search for specific user accounts</span></span>

1. <span data-ttu-id="9250b-144">Sélectionnez **Utilisateur** dans le menu déroulant **de** la barre de recherche.</span><span class="sxs-lookup"><span data-stu-id="9250b-144">Select **User** from the **Search bar** drop-down menu.</span></span>
2. <span data-ttu-id="9250b-145">Entrez le compte d’utilisateur dans le **champ** Recherche.</span><span class="sxs-lookup"><span data-stu-id="9250b-145">Enter the user account in the **Search** field.</span></span>
3. <span data-ttu-id="9250b-146">Cliquez sur l’icône de recherche ou appuyez sur **Entrée.**</span><span class="sxs-lookup"><span data-stu-id="9250b-146">Click the search icon or press **Enter**.</span></span>

<span data-ttu-id="9250b-147">Une liste d’utilisateurs correspondant au texte de la requête s’affiche.</span><span class="sxs-lookup"><span data-stu-id="9250b-147">A list of users matching the query text is displayed.</span></span> <span data-ttu-id="9250b-148">Vous verrez le domaine et le nom du compte d’utilisateur, la dernière fois que le compte d’utilisateur a été vu, ainsi que le nombre total d’appareils sur qui il a été connecté au cours des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="9250b-148">You'll see the user account's domain and name, when the user account was last seen, and the total number of devices it was observed logged on to in the last 30 days.</span></span>

<span data-ttu-id="9250b-149">Vous pouvez filtrer les résultats selon les périodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="9250b-149">You can filter the results by the following time periods:</span></span>

- <span data-ttu-id="9250b-150">1 jour</span><span class="sxs-lookup"><span data-stu-id="9250b-150">1 day</span></span>
- <span data-ttu-id="9250b-151">3 jours</span><span class="sxs-lookup"><span data-stu-id="9250b-151">3 days</span></span>
- <span data-ttu-id="9250b-152">7 jours</span><span class="sxs-lookup"><span data-stu-id="9250b-152">7 days</span></span>
- <span data-ttu-id="9250b-153">30 jours</span><span class="sxs-lookup"><span data-stu-id="9250b-153">30 days</span></span>
- <span data-ttu-id="9250b-154">6 mois</span><span class="sxs-lookup"><span data-stu-id="9250b-154">6 months</span></span>

## <a name="related-topics"></a><span data-ttu-id="9250b-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9250b-155">Related topics</span></span>

- [<span data-ttu-id="9250b-156">Afficher et organiser la file d’attente des alertes microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="9250b-156">View and organize the Microsoft Defender for Endpoint Alerts queue</span></span>](alerts-queue.md)
- [<span data-ttu-id="9250b-157">Gérer les alertes microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="9250b-157">Manage Microsoft Defender for Endpoint alerts</span></span>](manage-alerts.md)
- [<span data-ttu-id="9250b-158">Examiner microsoft Defender pour les alertes de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="9250b-158">Investigate Microsoft Defender for Endpoint alerts</span></span>](investigate-alerts.md)
- [<span data-ttu-id="9250b-159">Examiner un fichier associé à une alerte Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="9250b-159">Investigate a file associated with a Defender for Endpoint alert</span></span>](investigate-files.md)
- [<span data-ttu-id="9250b-160">Examiner les appareils dans la liste Defender pour les appareils de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="9250b-160">Investigate devices in the Defender for Endpoint Devices list</span></span>](investigate-machines.md)
- [<span data-ttu-id="9250b-161">Examiner une adresse IP associée à une alerte Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="9250b-161">Investigate an IP address associated with a Defender for Endpoint alert</span></span>](investigate-ip.md)
- [<span data-ttu-id="9250b-162">Examiner un domaine associé à une alerte Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="9250b-162">Investigate a domain associated with a Defender for Endpoint alert</span></span>](investigate-domain.md)
