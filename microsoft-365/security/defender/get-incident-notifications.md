---
title: Obtenir des notifications d'incident par courrier électronique dans Microsoft 365 Defender
description: Découvrez comment créer des règles pour obtenir des notifications par courrier électronique pour les incidents dans Microsoft 365 Defender
keywords: incident, e-mail, notfications de courrier électronique, configurer, utilisateurs, boîte aux lettres, courrier électronique, incidents, analyser, réponse
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: conceptual
search.appverid:
- MOE150
- MET150
ms.technology: m365d
ms.openlocfilehash: 7ba21e08f72760654993335764df00e78abc87b2
ms.sourcegitcommit: 4076b43a4b661de029f6307ddc1a989ab3108edb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "51939717"
---
# <a name="get-incident-notifications-by-email"></a><span data-ttu-id="0f87f-104">Obtenir des notifications d'incident par courrier électronique</span><span class="sxs-lookup"><span data-stu-id="0f87f-104">Get incident notifications by email</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="0f87f-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="0f87f-105">**Applies to:**</span></span>
- <span data-ttu-id="0f87f-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="0f87f-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="0f87f-107">Vous pouvez configurer Microsoft 365 Defender pour informer votre personnel par courrier électronique des nouveaux incidents ou des mises à jour des incidents existants.</span><span class="sxs-lookup"><span data-stu-id="0f87f-107">You can set up Microsoft 365 Defender to notify your staff with an email about new incidents or updates to existing incidents.</span></span> <span data-ttu-id="0f87f-108">Vous pouvez choisir d'obtenir des notifications basées sur :</span><span class="sxs-lookup"><span data-stu-id="0f87f-108">You can choose to get notifications based on:</span></span>

- <span data-ttu-id="0f87f-109">Gravité de l'incident.</span><span class="sxs-lookup"><span data-stu-id="0f87f-109">Incident severity.</span></span>
- <span data-ttu-id="0f87f-110">Groupe d'appareils.</span><span class="sxs-lookup"><span data-stu-id="0f87f-110">Device group.</span></span>
- <span data-ttu-id="0f87f-111">Uniquement sur la première mise à jour par incident.</span><span class="sxs-lookup"><span data-stu-id="0f87f-111">Only on the first update per incident.</span></span>

<span data-ttu-id="0f87f-112">La notification par courrier électronique contient des détails importants sur l'incident, tels que le nom de l'incident, sa gravité et ses catégories, entre autres.</span><span class="sxs-lookup"><span data-stu-id="0f87f-112">The email notification contains important details about the incident like the incident name, severity, and categories, among others.</span></span> <span data-ttu-id="0f87f-113">Vous pouvez également passer directement à l'incident et démarrer votre analyse immédiatement.</span><span class="sxs-lookup"><span data-stu-id="0f87f-113">You can also go directly to the incident and start your analysis right away.</span></span> <span data-ttu-id="0f87f-114">Pour plus d'informations, voir [Analyser les incidents.](investigate-incidents.md)</span><span class="sxs-lookup"><span data-stu-id="0f87f-114">For more information, see [Analyze incidents](investigate-incidents.md).</span></span>

<span data-ttu-id="0f87f-115">Vous pouvez ajouter ou supprimer des destinataires dans les notifications par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="0f87f-115">You can add or remove recipients in the email notifications.</span></span> <span data-ttu-id="0f87f-116">Les nouveaux destinataires sont avertis des incidents après leur ajout.</span><span class="sxs-lookup"><span data-stu-id="0f87f-116">New recipients get notified about incidents after they're added.</span></span> 

>[!NOTE]
><span data-ttu-id="0f87f-117">Vous avez besoin de l'autorisation « Gérer les paramètres de sécurité » pour configurer les paramètres de notification par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="0f87f-117">You need the 'Manage security settings' permission to configure email notification settings.</span></span> <span data-ttu-id="0f87f-118">Si vous avez choisi d'utiliser la gestion des autorisations de base, les utilisateurs ayant des rôles Administrateur de sécurité ou Administrateur général peuvent configurer des notifications par courrier électronique pour vous.</span><span class="sxs-lookup"><span data-stu-id="0f87f-118">If you've chosen to use basic permissions management, users with Security Administrator or Global Administrator roles can configure email notifications for you.</span></span> <br> <br>
<span data-ttu-id="0f87f-119">De même, si votre organisation utilise le contrôle d'accès basé sur un rôle (RBAC), vous pouvez uniquement créer, modifier, supprimer et recevoir des notifications basées sur les groupes d'appareils que vous êtes autorisé à gérer.</span><span class="sxs-lookup"><span data-stu-id="0f87f-119">Likewise, if your organization is using role-based access control (RBAC), you can only create, edit, delete, and receive notifications based on device groups that you are allowed to manage.</span></span>

## <a name="create-a-rule-for-email-notifications"></a><span data-ttu-id="0f87f-120">Créer une règle pour les notifications par courrier électronique</span><span class="sxs-lookup"><span data-stu-id="0f87f-120">Create a rule for email notifications</span></span>

<span data-ttu-id="0f87f-121">Suivez ces étapes pour créer une règle et personnaliser les paramètres de notification par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="0f87f-121">Follow these steps to create a new rule and customize email notification settings.</span></span>

1. <span data-ttu-id="0f87f-122">Dans le volet de navigation, sélectionnez Paramètres > notifications d'incident microsoft **365 Defender > incident.**</span><span class="sxs-lookup"><span data-stu-id="0f87f-122">In the navigation pane, select **Settings > Microsoft 365 Defender > Incident email notifications**.</span></span>
2. <span data-ttu-id="0f87f-123">Sélectionnez **Ajouter un élément.**</span><span class="sxs-lookup"><span data-stu-id="0f87f-123">Select **Add item**.</span></span>
3. <span data-ttu-id="0f87f-124">Dans la page **Informations de** base, tapez le nom de la règle et une description, puis sélectionnez **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="0f87f-124">On the **Basics** page, type the rule name and a description, and then select **Next**.</span></span>
4. <span data-ttu-id="0f87f-125">Dans la **page Paramètres de** notification, configurez :</span><span class="sxs-lookup"><span data-stu-id="0f87f-125">On the **Notification settings** page, configure:</span></span>
    - <span data-ttu-id="0f87f-126">**Gravité de l'alerte** : choisissez les gravités d'alerte qui déclencheront une notification d'incident.</span><span class="sxs-lookup"><span data-stu-id="0f87f-126">**Alert severity** - Choose the alert severities that will trigger an incident notification.</span></span> <span data-ttu-id="0f87f-127">Par exemple, si vous souhaitez uniquement être informé des incidents de gravité élevée, sélectionnez **Élevé**.</span><span class="sxs-lookup"><span data-stu-id="0f87f-127">For example, if you only want to be informed about high-severity incidents, select **High**.</span></span>
    - <span data-ttu-id="0f87f-128">**Étendue du groupe d'appareils** : vous pouvez spécifier tous les groupes d'appareils ou sélectionner dans la liste des groupes d'appareils de votre client.</span><span class="sxs-lookup"><span data-stu-id="0f87f-128">**Device group scope** - You can specify all device groups or select from the list of device groups in your tenant.</span></span>
    - <span data-ttu-id="0f87f-129">**Notifier uniquement lors de la** première occurrence par incident : sélectionnez si vous souhaitez recevoir une notification uniquement sur la première alerte qui correspond à vos autres sélections.</span><span class="sxs-lookup"><span data-stu-id="0f87f-129">**Only notify on first occurrence per incident** - Select if you want a notification only on the first alert that matches your other selections.</span></span> <span data-ttu-id="0f87f-130">Les mises à jour ou alertes ultérieures liées à l'incident n'envoient pas de notifications supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="0f87f-130">Later updates or alerts related to the incident won't send additional notifications.</span></span>
    - <span data-ttu-id="0f87f-131">**Inclure le nom de l'organisation dans l'e-mail** : sélectionnez si vous souhaitez que le nom de votre organisation apparaisse dans la notification par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="0f87f-131">**Include organization name in the email** - Select if you want your organization name to appear in the email notification.</span></span>
    - <span data-ttu-id="0f87f-132">**Inclure un** lien portail propre au client : sélectionnez si vous souhaitez ajouter un lien avec l'ID de client dans la notification par courrier électronique pour accéder à un client Microsoft 365 spécifique.</span><span class="sxs-lookup"><span data-stu-id="0f87f-132">**Include tenant-specific portal link** - Select if you want to add a link with the tenant ID in the email notification for access to a specific Microsoft 365 tenant.</span></span>

    :::image type="content" source="../../media/get-incident-notifications/incidents-ss-email-notification-settings.png" alt-text="Paramètres de notification pour les notifications d'incident par courrier électronique":::

5. <span data-ttu-id="0f87f-134">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0f87f-134">Select **Next**.</span></span> <span data-ttu-id="0f87f-135">Dans la page **Destinataires,** ajoutez les adresses de messagerie qui recevront les notifications d'incident.</span><span class="sxs-lookup"><span data-stu-id="0f87f-135">On the **Recipients** page, add the email addresses that will receive the incident notifications.</span></span> <span data-ttu-id="0f87f-136">Sélectionnez **Ajouter** après avoir tapé chaque nouvelle adresse de messagerie.</span><span class="sxs-lookup"><span data-stu-id="0f87f-136">Select **Add** after typing each new email address.</span></span> <span data-ttu-id="0f87f-137">Pour tester les notifications et vérifier que les destinataires les reçoivent dans les boîtes de réception, **sélectionnez Envoyer un message électronique de test.**</span><span class="sxs-lookup"><span data-stu-id="0f87f-137">To test notifications and ensure that the recipients receive them in the inboxes, select **Send test email**.</span></span> 
6. <span data-ttu-id="0f87f-138">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0f87f-138">Select **Next**.</span></span> <span data-ttu-id="0f87f-139">Dans la page **Examiner la règle,** examinez les paramètres de la règle, puis sélectionnez **Créer une règle.**</span><span class="sxs-lookup"><span data-stu-id="0f87f-139">On the **Review rule** page, review the settings of the rule, and then select **Create rule**.</span></span> <span data-ttu-id="0f87f-140">Les destinataires commenceront à recevoir des notifications d'incident par courrier électronique en fonction des paramètres.</span><span class="sxs-lookup"><span data-stu-id="0f87f-140">Recipients will start receiving incident notifications through email based on the settings.</span></span>

<span data-ttu-id="0f87f-141">Pour modifier une règle existante, sélectionnez-la dans la liste des règles.</span><span class="sxs-lookup"><span data-stu-id="0f87f-141">To edit an existing rule, select it from the list of rules.</span></span> <span data-ttu-id="0f87f-142">Dans le volet avec le  nom de la règle, sélectionnez Modifier la règle et a apporté vos modifications dans les pages De **base,** **Paramètres** de notification et **Destinataires.**</span><span class="sxs-lookup"><span data-stu-id="0f87f-142">On the pane with the rule name, select **Edit rule** and make your changes on the **Basics**, **Notification settings**, and **Recipients** pages.</span></span>

<span data-ttu-id="0f87f-143">Pour modifier une règle existante, sélectionnez-la dans la liste des règles.</span><span class="sxs-lookup"><span data-stu-id="0f87f-143">To edit an existing rule, select it from the list of rules.</span></span> <span data-ttu-id="0f87f-144">Dans le volet avec le nom de la règle, sélectionnez **Supprimer.**</span><span class="sxs-lookup"><span data-stu-id="0f87f-144">On the pane with the rule name, select **Delete**.</span></span>

## <a name="see-also"></a><span data-ttu-id="0f87f-145">Articles associés</span><span class="sxs-lookup"><span data-stu-id="0f87f-145">See also</span></span>
- [<span data-ttu-id="0f87f-146">Vue d’ensemble des incidents</span><span class="sxs-lookup"><span data-stu-id="0f87f-146">Incidents overview</span></span>](incidents-overview.md)
- [<span data-ttu-id="0f87f-147">Hiérarchiser les incidents</span><span class="sxs-lookup"><span data-stu-id="0f87f-147">Prioritize incidents</span></span>](incident-queue.md)
- [<span data-ttu-id="0f87f-148">Analyser les incidents</span><span class="sxs-lookup"><span data-stu-id="0f87f-148">Analyze incidents</span></span>](investigate-incidents.md)
