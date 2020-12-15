---
title: Obtenir des notifications d’incident dans Microsoft 365 Defender
description: Découvrez comment créer des règles pour obtenir des notifications par courrier électronique pour les incidents dans Microsoft 365 Defender
keywords: incident, e-mail, courrier électronique, notfications, configurer, utilisateurs, boîte aux lettres, e-mail, incidents
search.product: eADQiWindows 10XVcnh
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: maccruz
author: schmurky
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: conceptual
search.appverid:
- MOE150
- MET150
ms.openlocfilehash: 3af1dcfec165c88a18cbc0d8cbf6866bb6398adc
ms.sourcegitcommit: 1a9f0f878c045e1ddd59088ca2a94397605a242a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "49668198"
---
# <a name="get-incident-notifications-by-email"></a><span data-ttu-id="e2dc5-104">Obtenir des notifications d’incident par courrier électronique</span><span class="sxs-lookup"><span data-stu-id="e2dc5-104">Get incident notifications by email</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

>[!IMPORTANT]
> <span data-ttu-id="e2dc5-105">La fonctionnalité notifications par courrier électronique pour les incidents est actuellement en préversion publique.</span><span class="sxs-lookup"><span data-stu-id="e2dc5-105">The email notifications for incidents feature is currently in public preview.</span></span> <span data-ttu-id="e2dc5-106">Certaines informations sur cette fonctionnalité peuvent changer avant la disponibilité commerciale.</span><span class="sxs-lookup"><span data-stu-id="e2dc5-106">Some information about this feature may change before commercial availability.</span></span> <span data-ttu-id="e2dc5-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span><span class="sxs-lookup"><span data-stu-id="e2dc5-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

<span data-ttu-id="e2dc5-108">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="e2dc5-108">**Applies to:**</span></span>
- <span data-ttu-id="e2dc5-109">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="e2dc5-109">Microsoft 365 Defender</span></span>

<span data-ttu-id="e2dc5-110">Vous pouvez configurer Microsoft 365 Defender pour qu’il vous avertisse par courrier électronique chaque fois qu’il y a de nouveaux incidents ou de nouvelles mises à jour apportées aux incidents existants.</span><span class="sxs-lookup"><span data-stu-id="e2dc5-110">You can set up Microsoft 365 Defender to notify you by email every time there are new incidents or new updates to existing incidents.</span></span> 

<span data-ttu-id="e2dc5-111">Vous pouvez choisir d’obtenir des notifications en fonction de la gravité de l’incident ou du groupe d’appareils.</span><span class="sxs-lookup"><span data-stu-id="e2dc5-111">You can choose to get notifications based on incident severity or by device group.</span></span> <span data-ttu-id="e2dc5-112">Vous pouvez également choisir d’obtenir une notification uniquement lors de la première mise à jour par incident.</span><span class="sxs-lookup"><span data-stu-id="e2dc5-112">You can also choose to get a notification only on the first update per incident.</span></span>

<span data-ttu-id="e2dc5-113">Vous pouvez ajouter ou supprimer des destinataires dans les notifications par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="e2dc5-113">You can add or remove recipients in the email notifications.</span></span> <span data-ttu-id="e2dc5-114">Les destinataires nouvellement ajoutés reçoivent une notification sur les incidents une fois qu’ils ont été ajoutés.</span><span class="sxs-lookup"><span data-stu-id="e2dc5-114">Newly added recipients get notified about incidents after they're added.</span></span> 

<span data-ttu-id="e2dc5-115">La notification par courrier électronique contient des informations importantes sur l’incident, telles que le nom, la gravité et les catégories de l’incident, entre autres.</span><span class="sxs-lookup"><span data-stu-id="e2dc5-115">The email notification contains important details about the incident like the incident name, severity, and categories, among others.</span></span> <span data-ttu-id="e2dc5-116">Vous pouvez également accéder directement aux incidents afin de commencer immédiatement votre enquête.</span><span class="sxs-lookup"><span data-stu-id="e2dc5-116">You can also directly go to incidents so you can start your investigation right away.</span></span> <span data-ttu-id="e2dc5-117">Pour plus d’informations sur les incidents, consultez la rubrique [identifier les incidents dans Microsoft 365 Defender](https://docs.microsoft.com/microsoft-365/security/mtp/investigate-incidents).</span><span class="sxs-lookup"><span data-stu-id="e2dc5-117">For more on investigating incidents, see [Investigate incidents in Microsoft 365 Defender](https://docs.microsoft.com/microsoft-365/security/mtp/investigate-incidents).</span></span>

>[!NOTE]
><span data-ttu-id="e2dc5-118">Vous avez besoin des autorisations « gérer les paramètres de sécurité » pour configurer les paramètres de notification par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="e2dc5-118">You need 'Manage security settings' permissions to configure email notification settings.</span></span> <span data-ttu-id="e2dc5-119">Si vous avez choisi d’utiliser la gestion des autorisations de base, les utilisateurs disposant de rôles d’administrateur général ou d’administrateur de sécurité peuvent configurer des notifications par courrier électronique pour vous.</span><span class="sxs-lookup"><span data-stu-id="e2dc5-119">If you've chosen to use basic permissions management, users with Security Administrator or Global Administrator roles can configure email notifications for you.</span></span> <br> <br>
<span data-ttu-id="e2dc5-120">De même, si votre organisation utilise le contrôle d’accès basé sur un rôle (RBAC), vous pouvez uniquement créer, modifier, supprimer et recevoir des notifications basées sur les groupes d’appareils que vous êtes autorisé à gérer.</span><span class="sxs-lookup"><span data-stu-id="e2dc5-120">Likewise, if your organization is using role-based access control (RBAC), you can only create, edit, delete, and receive notifications based on device groups that you are allowed to manage.</span></span>

## <a name="create-rules-for-incident-notifications"></a><span data-ttu-id="e2dc5-121">Créer des règles pour les notifications d’incident</span><span class="sxs-lookup"><span data-stu-id="e2dc5-121">Create rules for incident notifications</span></span>

<span data-ttu-id="e2dc5-122">Pour configurer votre première notification par courrier électronique pour les incidents, créez une nouvelle règle et personnalisez les paramètres de notification par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="e2dc5-122">To set up your first email notification for incidents, create a new rule and customize email notification settings.</span></span>

1. <span data-ttu-id="e2dc5-123">Dans le volet de navigation, sélectionnez **paramètres**  >  **des notifications par courrier électronique des incidents**.</span><span class="sxs-lookup"><span data-stu-id="e2dc5-123">In the navigation pane, select **Settings** > **Incident email notifications**.</span></span>
2. <span data-ttu-id="e2dc5-124">Sélectionnez **Ajouter un élément**.</span><span class="sxs-lookup"><span data-stu-id="e2dc5-124">Select **Add item**.</span></span>
3. <span data-ttu-id="e2dc5-125">Attribuez un **nom à la** règle et fournissez une **Description**.</span><span class="sxs-lookup"><span data-stu-id="e2dc5-125">Give the rule a name in **Name** and supply a **Description**.</span></span>

    ![Fenêtre créer une règle pour le courrier électronique d’incident notifs](../../media/incidentemailnotif1.png) 
4. <span data-ttu-id="e2dc5-127">Sélectionnez **suivant** pour accéder aux **paramètres de notification**.</span><span class="sxs-lookup"><span data-stu-id="e2dc5-127">Select **Next** to go to **Notification settings**.</span></span> <span data-ttu-id="e2dc5-128">Vous pouvez spécifier les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="e2dc5-128">Here you can specify:</span></span>
    - <span data-ttu-id="e2dc5-129">**Gravité des alertes** : choisissez la gravité d’alerte qui déclenchera une notification d’incident.</span><span class="sxs-lookup"><span data-stu-id="e2dc5-129">**Alert severity** - Choose the alert severity that will trigger an incident notification.</span></span> <span data-ttu-id="e2dc5-130">Par exemple, si vous souhaitez uniquement être informé des incidents de gravité élevée, sélectionnez haute.</span><span class="sxs-lookup"><span data-stu-id="e2dc5-130">For example, if you only want to be informed about High severity incidents, select High.</span></span>
    - <span data-ttu-id="e2dc5-131">**Étendue du groupe d’appareils** : cette liste déroulante affiche tous les groupes d’appareils auxquels l’utilisateur peut accéder.</span><span class="sxs-lookup"><span data-stu-id="e2dc5-131">**Device group scope** - This dropdown displays all the device groups the user can access.</span></span> <span data-ttu-id="e2dc5-132">Sélectionnez les groupes de périphériques pour lesquels vous créez les règles de notification d’incident.</span><span class="sxs-lookup"><span data-stu-id="e2dc5-132">Select which device groups you're creating the incident notification rules for.</span></span>
    - <span data-ttu-id="e2dc5-133">Notification **uniquement lors de la première occurrence par incident** -la sélection de cette option envoie une notification par courrier électronique uniquement sur la première alerte correspondant à vos autres sélections.</span><span class="sxs-lookup"><span data-stu-id="e2dc5-133">**Only notify on first occurrence per incident** - Selecting this option will send an email notification only on the first alert that matches your other selections.</span></span> <span data-ttu-id="e2dc5-134">Les mises à jour ultérieures ou les alertes liées à l’incident ne déclencheront pas de notification.</span><span class="sxs-lookup"><span data-stu-id="e2dc5-134">Later updates or alerts related to the incident won't trigger a notification.</span></span>
    - <span data-ttu-id="e2dc5-135">**Inclure le nom** de l’Organisation : indique si le nom du client apparaît dans la notification par courrier électronique ou non.</span><span class="sxs-lookup"><span data-stu-id="e2dc5-135">**Include organization name** - Indicates whether the customer name appears on the email notification or not.</span></span>
    - <span data-ttu-id="e2dc5-136">**Inclure le lien portail propre au client** : ajoute un lien avec l’ID de client pour autoriser l’accès à un client spécifique.</span><span class="sxs-lookup"><span data-stu-id="e2dc5-136">**Include tenant-specific portal link** -  Adds a link with the tenant ID to allow access to a specific tenant.</span></span>
    
    ![Fenêtre des paramètres de notification pour le courrier électronique d’incident notifs](../../media/incidentemailnotif2.png)
5. <span data-ttu-id="e2dc5-138">Sélectionnez **suivant** pour accéder à la section **destinataires** .</span><span class="sxs-lookup"><span data-stu-id="e2dc5-138">Select **Next** to go the **Recipients** section.</span></span> <span data-ttu-id="e2dc5-139">Ici, vous pouvez spécifier les adresses de messagerie qui recevront les notifications par courrier électronique de l’incident.</span><span class="sxs-lookup"><span data-stu-id="e2dc5-139">Here you can specify email addresses that will receive the incident email notifications.</span></span> <span data-ttu-id="e2dc5-140">Sélectionnez **Ajouter un destinataire** après avoir tapé toutes les adresses de messagerie.</span><span class="sxs-lookup"><span data-stu-id="e2dc5-140">Select **Add a recipient** after typing every email address.</span></span>

    ![Fenêtre Ajouter des destinataires pour le courrier électronique d’incident notifs](../../media/incidentemailnotif3.png) 

6. <span data-ttu-id="e2dc5-142">Enfin, sélectionnez **suivant** pour accéder à la **règle de révision** afin de pouvoir voir tous les paramètres associés à votre nouvelle règle.</span><span class="sxs-lookup"><span data-stu-id="e2dc5-142">Finally, select **Next** to go to **Review rule** so you can see all the settings associated with your new rule.</span></span> <span data-ttu-id="e2dc5-143">Les destinataires commenceront à recevoir des notifications d’incidents par courrier électronique en fonction des paramètres.</span><span class="sxs-lookup"><span data-stu-id="e2dc5-143">Recipients will start receiving incident notifications through email based on the settings.</span></span>

## <a name="see-also"></a><span data-ttu-id="e2dc5-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2dc5-144">See also</span></span>
- [<span data-ttu-id="e2dc5-145">Présentation des incidents dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="e2dc5-145">Incidents overview in Microsoft 365 Defender</span></span>](https://docs.microsoft.com/microsoft-365/security/mtp/incidents-overview)
- [<span data-ttu-id="e2dc5-146">Hiérarchisation des incidents dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="e2dc5-146">Prioritize incidents in Microsoft 365 Defender</span></span>](https://docs.microsoft.com/microsoft-365/security/mtp/incident-queue)
- [<span data-ttu-id="e2dc5-147">Enquête sur les incidents dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="e2dc5-147">Investigate incidents in Microsoft 365 Defender</span></span>](https://docs.microsoft.com/microsoft-365/security/mtp/investigate-incidents)

