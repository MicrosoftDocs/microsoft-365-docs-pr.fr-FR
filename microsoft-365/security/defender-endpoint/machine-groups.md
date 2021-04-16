---
title: Créer et gérer des groupes d'appareils dans Microsoft Defender pour le point de terminaison
description: Créer des groupes d'appareils et définir des niveaux de correction automatisés sur ces derniers en confint les règles qui s'appliquent au groupe
keywords: groupes d'appareils, groupes, correction, niveau, règles, groupe aad, rôle, attribuer, classement
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
ms.openlocfilehash: acd24e5c87a74bbb32835ec170a121c5c0b6bb33
ms.sourcegitcommit: 22505ce322f68a2d0ce70d71caf3b0a657fa838a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2021
ms.locfileid: "51860302"
---
# <a name="create-and-manage-device-groups"></a><span data-ttu-id="499e0-104">Créer et gérer des groupes d’appareils</span><span class="sxs-lookup"><span data-stu-id="499e0-104">Create and manage device groups</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="499e0-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="499e0-105">**Applies to:**</span></span>
- <span data-ttu-id="499e0-106">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="499e0-106">Azure Active Directory</span></span>
- <span data-ttu-id="499e0-107">Office 365</span><span class="sxs-lookup"><span data-stu-id="499e0-107">Office 365</span></span>

> <span data-ttu-id="499e0-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="499e0-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="499e0-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="499e0-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)


<span data-ttu-id="499e0-110">Dans un scénario d'entreprise, un ensemble d'appareils est généralement affecté aux équipes chargées des opérations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="499e0-110">In an enterprise scenario, security operation teams are typically assigned a set of devices.</span></span> <span data-ttu-id="499e0-111">Ces appareils sont regroupés en fonction d'un ensemble d'attributs tels que leurs domaines, noms d'ordinateur ou balises désignées.</span><span class="sxs-lookup"><span data-stu-id="499e0-111">These devices are grouped together based on a set of attributes such as their domains, computer names, or designated tags.</span></span>

<span data-ttu-id="499e0-112">Dans Microsoft Defender for Endpoint, vous pouvez créer des groupes d'appareils et les utiliser pour :</span><span class="sxs-lookup"><span data-stu-id="499e0-112">In Microsoft Defender for Endpoint, you can create device groups and use them to:</span></span>
- <span data-ttu-id="499e0-113">Limiter l'accès aux alertes et données associées à des groupes d'utilisateurs Azure AD spécifiques avec [des rôles RBAC attribués](rbac.md)</span><span class="sxs-lookup"><span data-stu-id="499e0-113">Limit access to related alerts and data to specific Azure AD user groups with [assigned RBAC roles](rbac.md)</span></span> 
- <span data-ttu-id="499e0-114">Configurer différents paramètres de correction automatique pour différents ensembles d'appareils</span><span class="sxs-lookup"><span data-stu-id="499e0-114">Configure different auto-remediation settings for different sets of devices</span></span>
- <span data-ttu-id="499e0-115">Affecter des niveaux de correction spécifiques à appliquer lors d'examens automatisés</span><span class="sxs-lookup"><span data-stu-id="499e0-115">Assign specific remediation levels to apply during automated investigations</span></span>
- <span data-ttu-id="499e0-116">Dans le cas d'un examen, filtrez la liste **Appareils** sur des groupes d'appareils spécifiques à l'aide du **filtre** Groupe.</span><span class="sxs-lookup"><span data-stu-id="499e0-116">In an investigation, filter the **Devices list** to just specific device groups by using the **Group** filter.</span></span>

<span data-ttu-id="499e0-117">Vous pouvez créer des groupes d'appareils dans le contexte de l'accès basé sur les rôles (RBAC) pour contrôler qui peut prendre des mesures spécifiques ou voir les informations en attribuant le ou les groupes d'appareils à un groupe d'utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="499e0-117">You can create device groups in the context of role-based access (RBAC) to control who can take specific action or see information by assigning the device group(s) to a user group.</span></span> <span data-ttu-id="499e0-118">Pour plus d'informations, voir [Gérer l'accès au portail à l'aide du contrôle d'accès basé sur les rôles.](rbac.md)</span><span class="sxs-lookup"><span data-stu-id="499e0-118">For more information, see [Manage portal access using role-based access control](rbac.md).</span></span>

>[!TIP]
> <span data-ttu-id="499e0-119">Pour une vue d'ensemble de l'application RBAC, lisez : votre SOC fonctionne-t-il [à plat avec RBAC](https://techcommunity.microsoft.com/t5/Windows-Defender-ATP/Is-your-SOC-running-flat-with-limited-RBAC/ba-p/320015).</span><span class="sxs-lookup"><span data-stu-id="499e0-119">For a comprehensive look into RBAC application, read: [Is your SOC running flat with RBAC](https://techcommunity.microsoft.com/t5/Windows-Defender-ATP/Is-your-SOC-running-flat-with-limited-RBAC/ba-p/320015).</span></span>

<span data-ttu-id="499e0-120">Dans le cadre du processus de création d'un groupe d'appareils, vous devez :</span><span class="sxs-lookup"><span data-stu-id="499e0-120">As part of the process of creating a device group, you'll:</span></span>
- <span data-ttu-id="499e0-121">Définissez le niveau de correction automatisé pour ce groupe.</span><span class="sxs-lookup"><span data-stu-id="499e0-121">Set the automated remediation level for that group.</span></span> <span data-ttu-id="499e0-122">Pour plus d'informations sur les niveaux de correction, voir [Utiliser l'examen automatisé pour examiner et corriger les menaces.](automated-investigations.md)</span><span class="sxs-lookup"><span data-stu-id="499e0-122">For more information on remediation levels, see [Use Automated investigation to investigate and remediate threats](automated-investigations.md).</span></span>
- <span data-ttu-id="499e0-123">Spécifiez la règle correspondante qui détermine quel groupe d'appareils appartient au groupe en fonction du nom de l'appareil, du domaine, des balises et de la plateforme du système d'exploitation.</span><span class="sxs-lookup"><span data-stu-id="499e0-123">Specify the matching rule that determines which device group belongs to the group based on the device name, domain, tags, and OS platform.</span></span> <span data-ttu-id="499e0-124">Si un appareil est également en correspondance avec d'autres groupes, il est ajouté uniquement au groupe d'appareils le plus élevé.</span><span class="sxs-lookup"><span data-stu-id="499e0-124">If a device is also matched to other groups, it is added only to the highest ranked device group.</span></span>
- <span data-ttu-id="499e0-125">Sélectionnez le groupe d'utilisateurs Azure AD qui doit avoir accès au groupe d'appareils.</span><span class="sxs-lookup"><span data-stu-id="499e0-125">Select the Azure AD user group that should have access to the device group.</span></span>
- <span data-ttu-id="499e0-126">Classer le groupe d'appareils par rapport aux autres groupes après sa création.</span><span class="sxs-lookup"><span data-stu-id="499e0-126">Rank the device group relative to other groups after it is created.</span></span>

>[!NOTE]
><span data-ttu-id="499e0-127">Un groupe d'appareils est accessible à tous les utilisateurs si vous n'y affectez aucun groupe Azure AD.</span><span class="sxs-lookup"><span data-stu-id="499e0-127">A device group is accessible to all users if you don’t assign any Azure AD groups to it.</span></span>

## <a name="create-a-device-group"></a><span data-ttu-id="499e0-128">Créer un groupe d'appareils</span><span class="sxs-lookup"><span data-stu-id="499e0-128">Create a device group</span></span>

1. <span data-ttu-id="499e0-129">Dans le volet de navigation, sélectionnez **Groupes d'appareils**  >  **Paramètres.**</span><span class="sxs-lookup"><span data-stu-id="499e0-129">In the navigation pane, select **Settings** > **Device groups**.</span></span>

2. <span data-ttu-id="499e0-130">Cliquez **sur Ajouter un groupe d'appareils.**</span><span class="sxs-lookup"><span data-stu-id="499e0-130">Click **Add device group**.</span></span>

3. <span data-ttu-id="499e0-131">Entrez le nom du groupe et les paramètres d'automatisation et spécifiez la règle correspondante qui détermine quels appareils appartiennent au groupe.</span><span class="sxs-lookup"><span data-stu-id="499e0-131">Enter the group name and automation settings and specify the matching rule that determines which devices belong to the group.</span></span> <span data-ttu-id="499e0-132">Découvrez [comment l'enquête automatisée démarre.](automated-investigations.md#how-the-automated-investigation-starts)</span><span class="sxs-lookup"><span data-stu-id="499e0-132">See [How the automated investigation starts](automated-investigations.md#how-the-automated-investigation-starts).</span></span>

    >[!TIP]
    ><span data-ttu-id="499e0-133">Si vous souhaitez grouper des appareils par unité d'organisation, vous pouvez configurer la clé de Registre pour l'affiliation au groupe.</span><span class="sxs-lookup"><span data-stu-id="499e0-133">If you want to group devices by organizational unit, you can configure the registry key for the group affiliation.</span></span> <span data-ttu-id="499e0-134">Pour plus d'informations sur le marquage des appareils, voir [Créer et gérer des balises d'appareil.](machine-tags.md)</span><span class="sxs-lookup"><span data-stu-id="499e0-134">For more information on device tagging, see [Create and manage device tags](machine-tags.md).</span></span>

4. <span data-ttu-id="499e0-135">Affichez un aperçu de plusieurs appareils qui seront en correspondance avec cette règle.</span><span class="sxs-lookup"><span data-stu-id="499e0-135">Preview several devices that will be matched by this rule.</span></span> <span data-ttu-id="499e0-136">Si vous êtes satisfait de la règle, cliquez sur **l'onglet Accès** utilisateur.</span><span class="sxs-lookup"><span data-stu-id="499e0-136">If you are satisfied with the rule, click the **User access** tab.</span></span>

5. <span data-ttu-id="499e0-137">Affectez les groupes d'utilisateurs qui peuvent accéder au groupe d'appareils que vous avez créé.</span><span class="sxs-lookup"><span data-stu-id="499e0-137">Assign the user groups that can access the device group you created.</span></span>

    >[!NOTE]
    ><span data-ttu-id="499e0-138">Vous pouvez uniquement accorder l'accès aux groupes d'utilisateurs Azure AD affectés à des rôles RBAC.</span><span class="sxs-lookup"><span data-stu-id="499e0-138">You can only grant access to Azure AD user groups that have been assigned to RBAC roles.</span></span>

6. <span data-ttu-id="499e0-139">Cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="499e0-139">Click **Close**.</span></span> <span data-ttu-id="499e0-140">Les modifications de configuration sont appliquées.</span><span class="sxs-lookup"><span data-stu-id="499e0-140">The configuration changes are applied.</span></span>

## <a name="manage-device-groups"></a><span data-ttu-id="499e0-141">Gérer les groupes d'appareils</span><span class="sxs-lookup"><span data-stu-id="499e0-141">Manage device groups</span></span>

<span data-ttu-id="499e0-142">Vous pouvez promouvoir ou rétrograder le rang d'un groupe d'appareils afin qu'il soit plus ou moins prioritaire lors de la mise en correspondance.</span><span class="sxs-lookup"><span data-stu-id="499e0-142">You can promote or demote the rank of a device group so that it is given higher or lower priority during matching.</span></span> <span data-ttu-id="499e0-143">Lorsqu'un appareil est en correspondance avec plusieurs groupes, il est ajouté uniquement au groupe le plus élevé.</span><span class="sxs-lookup"><span data-stu-id="499e0-143">When a device is matched to more than one group, it is added only to the highest ranked group.</span></span> <span data-ttu-id="499e0-144">Vous pouvez également modifier et supprimer des groupes.</span><span class="sxs-lookup"><span data-stu-id="499e0-144">You can also edit and delete groups.</span></span>

>[!WARNING]
><span data-ttu-id="499e0-145">La suppression d'un groupe d'appareils peut affecter les règles de notification par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="499e0-145">Deleting a device group may affect email notification rules.</span></span> <span data-ttu-id="499e0-146">Si un groupe d'appareils est configuré sous une règle de notification par courrier électronique, il sera supprimé de cette règle.</span><span class="sxs-lookup"><span data-stu-id="499e0-146">If a device group is configured under an email notification rule, it will be removed from that rule.</span></span> <span data-ttu-id="499e0-147">Si le groupe d'appareils est le seul groupe configuré pour une notification par courrier électronique, cette règle de notification par courrier électronique est supprimée avec le groupe d'appareils.</span><span class="sxs-lookup"><span data-stu-id="499e0-147">If the device group is the only group configured for an email notification, that email notification rule will be deleted along with the device group.</span></span>

<span data-ttu-id="499e0-148">Par défaut, les groupes d'appareils sont accessibles à tous les utilisateurs ayant accès au portail.</span><span class="sxs-lookup"><span data-stu-id="499e0-148">By default, device groups are accessible to all users with portal access.</span></span> <span data-ttu-id="499e0-149">Vous pouvez modifier le comportement par défaut en attribuant des groupes d'utilisateurs Azure AD au groupe d'appareils.</span><span class="sxs-lookup"><span data-stu-id="499e0-149">You can change the default behavior by assigning Azure AD user groups to the device group.</span></span>

<span data-ttu-id="499e0-150">Les appareils qui ne correspondent à aucun groupe sont ajoutés au groupe Appareils non regroupés (par défaut).</span><span class="sxs-lookup"><span data-stu-id="499e0-150">Devices that are not matched to any groups are added to Ungrouped devices (default) group.</span></span> <span data-ttu-id="499e0-151">Vous ne pouvez pas modifier le rang de ce groupe ou le supprimer.</span><span class="sxs-lookup"><span data-stu-id="499e0-151">You cannot change the rank of this group or delete it.</span></span> <span data-ttu-id="499e0-152">Toutefois, vous pouvez modifier le niveau de correction de ce groupe et définir les groupes d'utilisateurs Azure AD qui peuvent accéder à ce groupe.</span><span class="sxs-lookup"><span data-stu-id="499e0-152">However, you can change the remediation level of this group, and define the Azure AD user groups that can access this group.</span></span>

>[!NOTE]
> <span data-ttu-id="499e0-153">L'application de modifications à la configuration du groupe d'appareils peut prendre jusqu'à plusieurs minutes.</span><span class="sxs-lookup"><span data-stu-id="499e0-153">Applying changes to device group configuration may take up to several minutes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="499e0-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="499e0-154">Related topics</span></span>

- [<span data-ttu-id="499e0-155">Gérer l'accès au portail à l'aide du contrôle d'accès basé sur un rôle</span><span class="sxs-lookup"><span data-stu-id="499e0-155">Manage portal access using role-based based access control</span></span>](rbac.md)
- [<span data-ttu-id="499e0-156">Créer et gérer des balises d’appareils</span><span class="sxs-lookup"><span data-stu-id="499e0-156">Create and manage device tags</span></span>](machine-tags.md)
- [<span data-ttu-id="499e0-157">Obtenir la liste des groupes d'appareils client à l'aide de l'API Graph</span><span class="sxs-lookup"><span data-stu-id="499e0-157">Get list of tenant device groups using Graph API</span></span>](https://docs.microsoft.com/graph/api/device-list-memberof)
