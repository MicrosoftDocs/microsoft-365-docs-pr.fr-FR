---
title: Configurer les notifications d’alerte dans Microsoft Defender pour le point de terminaison
description: Vous pouvez utiliser Microsoft Defender pour le point de terminaison pour configurer les paramètres de notification par courrier électronique pour les alertes de sécurité, en fonction de la gravité et d’autres critères.
keywords: notifications par courrier électronique, configurer les notifications d’alerte, Microsoft Defender pour le point de terminaison, Microsoft Defender pour les notifications de point de terminaison, Microsoft Defender pour les alertes de point de terminaison, Windows 10 Entreprise, Windows 10 Éducation
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
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: c60bed1fb2cc17c9f5dfbd1289ae5f5b5e13faec
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51933948"
---
# <a name="configure-alert-notifications-in-microsoft-defender-for-endpoint"></a><span data-ttu-id="5c6df-104">Configurer les notifications d’alerte dans Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="5c6df-104">Configure alert notifications in Microsoft Defender for Endpoint</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="5c6df-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="5c6df-105">**Applies to:**</span></span>
- [<span data-ttu-id="5c6df-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="5c6df-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="5c6df-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="5c6df-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="5c6df-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="5c6df-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="5c6df-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="5c6df-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-emailconfig-abovefoldlink)

<span data-ttu-id="5c6df-110">Vous pouvez configurer Defender pour le point de terminaison pour envoyer des notifications par courrier électronique aux destinataires spécifiés pour les nouvelles alertes.</span><span class="sxs-lookup"><span data-stu-id="5c6df-110">You can configure Defender for Endpoint to send email notifications to specified recipients for new alerts.</span></span> <span data-ttu-id="5c6df-111">Cette fonctionnalité vous permet d’identifier un groupe de personnes qui seront immédiatement informées et qui pourront agir sur les alertes en fonction de leur gravité.</span><span class="sxs-lookup"><span data-stu-id="5c6df-111">This feature enables you to identify a group of individuals who will immediately be informed and can act on alerts based on their severity.</span></span>

> [!NOTE]
> <span data-ttu-id="5c6df-112">Seuls les utilisateurs ayant des autorisations « Gérer les paramètres de sécurité » peuvent configurer des notifications par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="5c6df-112">Only users with 'Manage security settings' permissions can configure email notifications.</span></span> <span data-ttu-id="5c6df-113">Si vous avez choisi d’utiliser la gestion des autorisations de base, les utilisateurs ayant des rôles Administrateur de sécurité ou Administrateur général peuvent configurer des notifications par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="5c6df-113">If you've chosen to use basic permissions management, users with Security Administrator or Global Administrator roles can configure email notifications.</span></span>

<span data-ttu-id="5c6df-114">Vous pouvez définir les niveaux de gravité des alertes qui déclenchent des notifications.</span><span class="sxs-lookup"><span data-stu-id="5c6df-114">You can set the alert severity levels that trigger notifications.</span></span> <span data-ttu-id="5c6df-115">Vous pouvez également ajouter ou supprimer des destinataires de la notification par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="5c6df-115">You can also add or remove recipients of the email notification.</span></span> <span data-ttu-id="5c6df-116">Les nouveaux destinataires sont avertis des alertes déclenchées après leur ajout.</span><span class="sxs-lookup"><span data-stu-id="5c6df-116">New recipients get notified about alerts triggered after they're added.</span></span> <span data-ttu-id="5c6df-117">Pour plus d’informations sur les alertes, voir [Afficher et organiser la file d’attente des alertes.](alerts-queue.md)</span><span class="sxs-lookup"><span data-stu-id="5c6df-117">For more information about alerts, see [View and organize the Alerts queue](alerts-queue.md).</span></span>

<span data-ttu-id="5c6df-118">Si vous utilisez le contrôle d’accès basé sur un rôle (RBAC), les destinataires recevront uniquement des notifications basées sur les groupes d’appareils configurés dans la règle de notification.</span><span class="sxs-lookup"><span data-stu-id="5c6df-118">If you're using role-based access control (RBAC), recipients will only receive notifications based on the device groups that were configured in the notification rule.</span></span>
<span data-ttu-id="5c6df-119">Les utilisateurs ayant l’autorisation appropriée peuvent uniquement créer, modifier ou supprimer des notifications limitées à leur étendue de gestion des groupes d’appareils.</span><span class="sxs-lookup"><span data-stu-id="5c6df-119">Users with the proper permission can only create, edit, or delete notifications that are limited to their device group management scope.</span></span>
<span data-ttu-id="5c6df-120">Seuls les utilisateurs affectés au rôle d’administrateur général peuvent gérer les règles de notification configurées pour tous les groupes d’appareils.</span><span class="sxs-lookup"><span data-stu-id="5c6df-120">Only users assigned to the Global administrator role can manage notification rules that are configured for all device groups.</span></span>

<span data-ttu-id="5c6df-121">La notification par courrier électronique inclut des informations de base sur l’alerte et un lien vers le portail où vous pouvez faire des recherches plus approfondies.</span><span class="sxs-lookup"><span data-stu-id="5c6df-121">The email notification includes basic information about the alert and a link to the portal where you can do further investigation.</span></span>


## <a name="create-rules-for-alert-notifications"></a><span data-ttu-id="5c6df-122">Créer des règles pour les notifications d’alerte</span><span class="sxs-lookup"><span data-stu-id="5c6df-122">Create rules for alert notifications</span></span>
<span data-ttu-id="5c6df-123">Vous pouvez créer des règles qui déterminent les appareils et les gravités des alertes pour envoyer des notifications par courrier électronique pour les destinataires de la notification.</span><span class="sxs-lookup"><span data-stu-id="5c6df-123">You can create rules that determine the devices and alert severities to send email notifications for and the notification recipients.</span></span>


1. <span data-ttu-id="5c6df-124">Dans le volet de navigation, sélectionnez **Paramètres**  >  **notifications par courrier électronique.**</span><span class="sxs-lookup"><span data-stu-id="5c6df-124">In the navigation pane, select **Settings** > **Email notifications**.</span></span>

2. <span data-ttu-id="5c6df-125">Cliquez **sur Ajouter un élément.**</span><span class="sxs-lookup"><span data-stu-id="5c6df-125">Click **Add item**.</span></span>

3. <span data-ttu-id="5c6df-126">Spécifiez les informations générales :</span><span class="sxs-lookup"><span data-stu-id="5c6df-126">Specify the General information:</span></span>
    - <span data-ttu-id="5c6df-127">**Nom de la** règle : spécifiez un nom pour la règle de notification.</span><span class="sxs-lookup"><span data-stu-id="5c6df-127">**Rule name** - Specify a name for the notification rule.</span></span>
    - <span data-ttu-id="5c6df-128">**Inclure le nom de l’organisation** : spécifiez le nom du client qui apparaît dans la notification par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="5c6df-128">**Include organization name** - Specify the customer name that appears on the email notification.</span></span>
    - <span data-ttu-id="5c6df-129">**Inclure un lien portail propre au client** : ajoute un lien avec l’ID de client pour autoriser l’accès à un client spécifique.</span><span class="sxs-lookup"><span data-stu-id="5c6df-129">**Include tenant-specific portal link** - Adds a link with the tenant ID to allow access to a specific tenant.</span></span>
    - <span data-ttu-id="5c6df-130">**Inclure des informations sur l’appareil** : inclut le nom de l’appareil dans le corps de l’alerte par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="5c6df-130">**Include device information** - Includes the device name in the email alert body.</span></span>
    
        >[!NOTE]
        > <span data-ttu-id="5c6df-131">Ces informations peuvent être traitées par des serveurs de messagerie destinataire qui ne se trouve pas dans l’emplacement géographique que vous avez sélectionné pour vos données Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="5c6df-131">This information might be processed by recipient mail servers that ar not in the geographic location you have selected for your Defender for Endpoint data.</span></span>

    - <span data-ttu-id="5c6df-132">**Appareils** : choisissez d’avertir les destinataires pour les alertes sur tous les appareils (rôle d’administrateur général uniquement) ou sur des groupes d’appareils sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="5c6df-132">**Devices** - Choose whether to notify recipients for alerts on all devices (Global administrator role only) or on selected device groups.</span></span> <span data-ttu-id="5c6df-133">Pour plus d’informations, voir [Créer et gérer des groupes d’appareils.](machine-groups.md)</span><span class="sxs-lookup"><span data-stu-id="5c6df-133">For more information, see [Create and manage device groups](machine-groups.md).</span></span>
    - <span data-ttu-id="5c6df-134">**Gravité de l’alerte** : choisissez le niveau de gravité de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="5c6df-134">**Alert severity** - Choose the alert severity level.</span></span>

4. <span data-ttu-id="5c6df-135">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="5c6df-135">Click **Next**.</span></span>
    
5. <span data-ttu-id="5c6df-136">Entrez l’adresse e-mail du destinataire, puis cliquez **sur Ajouter un destinataire.**</span><span class="sxs-lookup"><span data-stu-id="5c6df-136">Enter the recipient's email address then click **Add recipient**.</span></span> <span data-ttu-id="5c6df-137">Vous pouvez ajouter plusieurs adresses e-mail.</span><span class="sxs-lookup"><span data-stu-id="5c6df-137">You can add multiple email addresses.</span></span>

6. <span data-ttu-id="5c6df-138">Vérifiez que les destinataires du courrier électronique peuvent recevoir les notifications par courrier électronique en sélectionnant **Envoyer un message électronique de test.**</span><span class="sxs-lookup"><span data-stu-id="5c6df-138">Check that email recipients can receive the email notifications by selecting **Send test email**.</span></span>

7. <span data-ttu-id="5c6df-139">Cliquez **sur Enregistrer la règle de notification.**</span><span class="sxs-lookup"><span data-stu-id="5c6df-139">Click **Save notification rule**.</span></span>

## <a name="edit-a-notification-rule"></a><span data-ttu-id="5c6df-140">Modifier une règle de notification</span><span class="sxs-lookup"><span data-stu-id="5c6df-140">Edit a notification rule</span></span>
1. <span data-ttu-id="5c6df-141">Sélectionnez la règle de notification que vous souhaitez modifier.</span><span class="sxs-lookup"><span data-stu-id="5c6df-141">Select the notification rule you'd like to edit.</span></span>

2. <span data-ttu-id="5c6df-142">Mettez à jour les informations des onglets Général et Destinataire.</span><span class="sxs-lookup"><span data-stu-id="5c6df-142">Update the General and Recipient tab information.</span></span>

3. <span data-ttu-id="5c6df-143">Cliquez **sur Enregistrer la règle de notification.**</span><span class="sxs-lookup"><span data-stu-id="5c6df-143">Click **Save notification rule**.</span></span>


## <a name="delete-notification-rule"></a><span data-ttu-id="5c6df-144">Supprimer une règle de notification</span><span class="sxs-lookup"><span data-stu-id="5c6df-144">Delete notification rule</span></span>

1. <span data-ttu-id="5c6df-145">Sélectionnez la règle de notification que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="5c6df-145">Select the notification rule you'd like to delete.</span></span>

2. <span data-ttu-id="5c6df-146">Cliquez sur **Supprimer**.</span><span class="sxs-lookup"><span data-stu-id="5c6df-146">Click **Delete**.</span></span>


## <a name="troubleshoot-email-notifications-for-alerts"></a><span data-ttu-id="5c6df-147">Résoudre les problèmes de notifications par courrier électronique pour les alertes</span><span class="sxs-lookup"><span data-stu-id="5c6df-147">Troubleshoot email notifications for alerts</span></span>
<span data-ttu-id="5c6df-148">Cette section répertorie les différents problèmes que vous pouvez rencontrer lors de l’utilisation de notifications par courrier électronique pour les alertes.</span><span class="sxs-lookup"><span data-stu-id="5c6df-148">This section lists various issues that you may encounter when using email notifications for alerts.</span></span>

<span data-ttu-id="5c6df-149">**Problème :** Les destinataires prévus signalent qu’ils n’ont pas reçu les notifications.</span><span class="sxs-lookup"><span data-stu-id="5c6df-149">**Problem:** Intended recipients report they're not getting the notifications.</span></span>

<span data-ttu-id="5c6df-150">**Solution :** Assurez-vous que les notifications ne sont pas bloquées par des filtres de courrier électronique :</span><span class="sxs-lookup"><span data-stu-id="5c6df-150">**Solution:** Make sure that the notifications aren't blocked by email filters:</span></span>

1. <span data-ttu-id="5c6df-151">Vérifiez que les notifications par courrier électronique defender pour point de terminaison ne sont pas envoyées au dossier Courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="5c6df-151">Check that the Defender for Endpoint email notifications aren't sent to the Junk Email folder.</span></span> <span data-ttu-id="5c6df-152">Marquez-les comme courrier non indésirable.</span><span class="sxs-lookup"><span data-stu-id="5c6df-152">Mark them as Not junk.</span></span>
2. <span data-ttu-id="5c6df-153">Vérifiez que votre produit de sécurité de messagerie ne bloque pas les notifications par courrier électronique de Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="5c6df-153">Check that your email security product isn't blocking the email notifications from Defender for Endpoint.</span></span>
3. <span data-ttu-id="5c6df-154">Vérifiez les règles de votre application de messagerie qui peuvent être en train d’capturer et de déplacer vos notifications par courrier électronique Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="5c6df-154">Check your email application rules that might be catching and moving your Defender for Endpoint email notifications.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c6df-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c6df-155">Related topics</span></span>
- [<span data-ttu-id="5c6df-156">Mettre à jour les paramètres de rétention des données</span><span class="sxs-lookup"><span data-stu-id="5c6df-156">Update data retention settings</span></span>](data-retention-settings.md)
- [<span data-ttu-id="5c6df-157">Configurer des fonctionnalités avancées</span><span class="sxs-lookup"><span data-stu-id="5c6df-157">Configure advanced features</span></span>](advanced-features.md)
