---
title: Obtenir des notifications d’incident dans Microsoft 365 Defender
description: Découvrez comment créer des règles pour obtenir des notifications par courrier électronique pour les incidents dans Microsoft 365 Defender
keywords: incident, courrier électronique, notfications de courrier électronique, configurer, utilisateurs, boîte aux lettres, courrier électronique, incidents
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
ms.openlocfilehash: f25be4de3f25db869957474c3cb32b20e9f7aa53
ms.sourcegitcommit: 88d358d778804b26d5e41c53b4f725d01a78112b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/13/2021
ms.locfileid: "49848890"
---
# <a name="get-incident-notifications-by-email"></a><span data-ttu-id="a3efb-104">Obtenir des notifications d’incident par courrier électronique</span><span class="sxs-lookup"><span data-stu-id="a3efb-104">Get incident notifications by email</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="a3efb-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="a3efb-105">**Applies to:**</span></span>
- <span data-ttu-id="a3efb-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="a3efb-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="a3efb-107">Vous pouvez configurer Microsoft 365 Defender pour vous avertir par courrier électronique chaque fois qu’il y a de nouveaux incidents ou de nouvelles mises à jour des incidents existants.</span><span class="sxs-lookup"><span data-stu-id="a3efb-107">You can set up Microsoft 365 Defender to notify you by email every time there are new incidents or new updates to existing incidents.</span></span> 

<span data-ttu-id="a3efb-108">Vous pouvez choisir d’obtenir des notifications en fonction de la gravité de l’incident ou par groupe d’appareils.</span><span class="sxs-lookup"><span data-stu-id="a3efb-108">You can choose to get notifications based on incident severity or by device group.</span></span> <span data-ttu-id="a3efb-109">Vous pouvez également choisir d’obtenir une notification uniquement sur la première mise à jour par incident.</span><span class="sxs-lookup"><span data-stu-id="a3efb-109">You can also choose to get a notification only on the first update per incident.</span></span>

<span data-ttu-id="a3efb-110">Vous pouvez ajouter ou supprimer des destinataires dans les notifications par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="a3efb-110">You can add or remove recipients in the email notifications.</span></span> <span data-ttu-id="a3efb-111">Les destinataires nouvellement ajoutés sont avertis des incidents après leur ajout.</span><span class="sxs-lookup"><span data-stu-id="a3efb-111">Newly added recipients get notified about incidents after they're added.</span></span> 

<span data-ttu-id="a3efb-112">La notification par courrier électronique contient des détails importants sur l’incident, tels que le nom de l’incident, sa gravité et ses catégories, entre autres.</span><span class="sxs-lookup"><span data-stu-id="a3efb-112">The email notification contains important details about the incident like the incident name, severity, and categories, among others.</span></span> <span data-ttu-id="a3efb-113">Vous pouvez également directement passer aux incidents afin de pouvoir lancer votre enquête immédiatement.</span><span class="sxs-lookup"><span data-stu-id="a3efb-113">You can also directly go to incidents so you can start your investigation right away.</span></span> <span data-ttu-id="a3efb-114">Pour plus d’informations sur l’examen des incidents, voir [Examiner les incidents dans Microsoft 365 Defender.](https://docs.microsoft.com/microsoft-365/security/mtp/investigate-incidents)</span><span class="sxs-lookup"><span data-stu-id="a3efb-114">For more on investigating incidents, see [Investigate incidents in Microsoft 365 Defender](https://docs.microsoft.com/microsoft-365/security/mtp/investigate-incidents).</span></span>

>[!NOTE]
><span data-ttu-id="a3efb-115">Vous avez besoin des autorisations « Gérer les paramètres de sécurité » pour configurer les paramètres de notification par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="a3efb-115">You need 'Manage security settings' permissions to configure email notification settings.</span></span> <span data-ttu-id="a3efb-116">Si vous avez choisi d’utiliser la gestion des autorisations de base, les utilisateurs ayant des rôles Administrateur de sécurité ou Administrateur général peuvent configurer des notifications par courrier électronique pour vous.</span><span class="sxs-lookup"><span data-stu-id="a3efb-116">If you've chosen to use basic permissions management, users with Security Administrator or Global Administrator roles can configure email notifications for you.</span></span> <br> <br>
<span data-ttu-id="a3efb-117">De même, si votre organisation utilise le contrôle d’accès basé sur un rôle (RBAC), vous pouvez uniquement créer, modifier, supprimer et recevoir des notifications basées sur les groupes d’appareils que vous êtes autorisé à gérer.</span><span class="sxs-lookup"><span data-stu-id="a3efb-117">Likewise, if your organization is using role-based access control (RBAC), you can only create, edit, delete, and receive notifications based on device groups that you are allowed to manage.</span></span>

## <a name="create-rules-for-incident-notifications"></a><span data-ttu-id="a3efb-118">Créer des règles pour les notifications d’incident</span><span class="sxs-lookup"><span data-stu-id="a3efb-118">Create rules for incident notifications</span></span>

<span data-ttu-id="a3efb-119">Pour configurer votre première notification par courrier électronique pour les incidents, créez une règle et personnalisez les paramètres de notification par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="a3efb-119">To set up your first email notification for incidents, create a new rule and customize email notification settings.</span></span>

1. <span data-ttu-id="a3efb-120">Dans le volet de navigation, sélectionnez **Notifications** par  >  **courrier électronique d’incident des paramètres.**</span><span class="sxs-lookup"><span data-stu-id="a3efb-120">In the navigation pane, select **Settings** > **Incident email notifications**.</span></span>
2. <span data-ttu-id="a3efb-121">Sélectionnez **Ajouter un élément.**</span><span class="sxs-lookup"><span data-stu-id="a3efb-121">Select **Add item**.</span></span>
3. <span data-ttu-id="a3efb-122">Donnez un nom à la règle dans **Nom** et fournissez une **description.**</span><span class="sxs-lookup"><span data-stu-id="a3efb-122">Give the rule a name in **Name** and supply a **Description**.</span></span>

    ![Créer une fenêtre de règle pour les notifs de courrier d’incident](../../media/incidentemailnotif1.png) 
4. <span data-ttu-id="a3efb-124">Sélectionnez **Suivant** pour aller aux **paramètres de notification.**</span><span class="sxs-lookup"><span data-stu-id="a3efb-124">Select **Next** to go to **Notification settings**.</span></span> <span data-ttu-id="a3efb-125">Ici, vous pouvez spécifier :</span><span class="sxs-lookup"><span data-stu-id="a3efb-125">Here you can specify:</span></span>
    - <span data-ttu-id="a3efb-126">**Gravité de l’alerte** : choisissez la gravité de l’alerte qui déclenchera une notification d’incident.</span><span class="sxs-lookup"><span data-stu-id="a3efb-126">**Alert severity** - Choose the alert severity that will trigger an incident notification.</span></span> <span data-ttu-id="a3efb-127">Par exemple, si vous souhaitez uniquement être informé des incidents de gravité élevée, sélectionnez Élevé.</span><span class="sxs-lookup"><span data-stu-id="a3efb-127">For example, if you only want to be informed about High severity incidents, select High.</span></span>
    - <span data-ttu-id="a3efb-128">**Étendue du groupe d’appareils** : cette dropdown affiche tous les groupes d’appareils accessibles par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a3efb-128">**Device group scope** - This dropdown displays all the device groups the user can access.</span></span> <span data-ttu-id="a3efb-129">Sélectionnez les groupes d’appareils pour lesquels vous créez les règles de notification d’incident.</span><span class="sxs-lookup"><span data-stu-id="a3efb-129">Select which device groups you're creating the incident notification rules for.</span></span>
    - <span data-ttu-id="a3efb-130">**Notifier uniquement lors** de la première occurrence par incident : la sélection de cette option envoie une notification par courrier électronique uniquement sur la première alerte qui correspond à vos autres sélections.</span><span class="sxs-lookup"><span data-stu-id="a3efb-130">**Only notify on first occurrence per incident** - Selecting this option will send an email notification only on the first alert that matches your other selections.</span></span> <span data-ttu-id="a3efb-131">Les mises à jour ou alertes ultérieures liées à l’incident ne déclenchent pas de notification.</span><span class="sxs-lookup"><span data-stu-id="a3efb-131">Later updates or alerts related to the incident won't trigger a notification.</span></span>
    - <span data-ttu-id="a3efb-132">**Inclure le nom de l’organisation** : indique si le nom du client apparaît ou non dans la notification par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="a3efb-132">**Include organization name** - Indicates whether the customer name appears on the email notification or not.</span></span>
    - <span data-ttu-id="a3efb-133">**Inclure un lien portail propre au client** : ajoute un lien avec l’ID de client pour autoriser l’accès à un client spécifique.</span><span class="sxs-lookup"><span data-stu-id="a3efb-133">**Include tenant-specific portal link** -  Adds a link with the tenant ID to allow access to a specific tenant.</span></span>
    
    ![Fenêtre des paramètres Notif pour les notifs de courrier électronique d’incident](../../media/incidentemailnotif2.png)
5. <span data-ttu-id="a3efb-135">Sélectionnez **Suivant** pour aller à la section **Destinataires.**</span><span class="sxs-lookup"><span data-stu-id="a3efb-135">Select **Next** to go the **Recipients** section.</span></span> <span data-ttu-id="a3efb-136">Ici, vous pouvez spécifier les adresses de messagerie qui recevront les notifications d’incident par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="a3efb-136">Here you can specify email addresses that will receive the incident email notifications.</span></span> <span data-ttu-id="a3efb-137">Sélectionnez **Ajouter un destinataire après** avoir tapé chaque adresse de messagerie.</span><span class="sxs-lookup"><span data-stu-id="a3efb-137">Select **Add a recipient** after typing every email address.</span></span>

    ![Fenêtre Ajouter des destinataires pour les notifs de courrier d’incident](../../media/incidentemailnotif3.png) 

6. <span data-ttu-id="a3efb-139">Enfin, **sélectionnez Suivant** pour passer **à la** règle de révision afin de voir tous les paramètres associés à votre nouvelle règle.</span><span class="sxs-lookup"><span data-stu-id="a3efb-139">Finally, select **Next** to go to **Review rule** so you can see all the settings associated with your new rule.</span></span> <span data-ttu-id="a3efb-140">Les destinataires commenceront à recevoir des notifications d’incident par courrier électronique en fonction des paramètres.</span><span class="sxs-lookup"><span data-stu-id="a3efb-140">Recipients will start receiving incident notifications through email based on the settings.</span></span>

## <a name="see-also"></a><span data-ttu-id="a3efb-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3efb-141">See also</span></span>
- [<span data-ttu-id="a3efb-142">Vue d’ensemble des incidents dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="a3efb-142">Incidents overview in Microsoft 365 Defender</span></span>](https://docs.microsoft.com/microsoft-365/security/mtp/incidents-overview)
- [<span data-ttu-id="a3efb-143">Hiérarchiser les incidents dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="a3efb-143">Prioritize incidents in Microsoft 365 Defender</span></span>](https://docs.microsoft.com/microsoft-365/security/mtp/incident-queue)
- [<span data-ttu-id="a3efb-144">Examiner les incidents dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="a3efb-144">Investigate incidents in Microsoft 365 Defender</span></span>](https://docs.microsoft.com/microsoft-365/security/mtp/investigate-incidents)

