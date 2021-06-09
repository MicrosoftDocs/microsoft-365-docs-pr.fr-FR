---
title: Créer et gérer des groupes d’appareils dans Microsoft Defender pour le point de terminaison
description: Créer des groupes d’appareils et définir des niveaux de correction automatisés sur ces derniers en confirmant les règles qui s’appliquent au groupe
keywords: groupes d’appareils, groupes, correction, niveau, règles, groupe aad, rôle, attribuer, classement
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
ms.openlocfilehash: d4f62acde4e7d790c7a7c8635f51c99f0823687d
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52842769"
---
# <a name="create-and-manage-device-groups"></a><span data-ttu-id="41310-104">Créer et gérer des groupes d’appareils</span><span class="sxs-lookup"><span data-stu-id="41310-104">Create and manage device groups</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="41310-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="41310-105">**Applies to:**</span></span>
- <span data-ttu-id="41310-106">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="41310-106">Azure Active Directory</span></span>
- <span data-ttu-id="41310-107">Office 365</span><span class="sxs-lookup"><span data-stu-id="41310-107">Office 365</span></span>

> <span data-ttu-id="41310-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="41310-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="41310-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="41310-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)


<span data-ttu-id="41310-110">Dans un scénario d’entreprise, un ensemble d’appareils est généralement affecté aux équipes chargées des opérations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="41310-110">In an enterprise scenario, security operation teams are typically assigned a set of devices.</span></span> <span data-ttu-id="41310-111">Ces appareils sont regroupés en fonction d’un ensemble d’attributs tels que leurs domaines, noms d’ordinateur ou balises désignées.</span><span class="sxs-lookup"><span data-stu-id="41310-111">These devices are grouped together based on a set of attributes such as their domains, computer names, or designated tags.</span></span>

<span data-ttu-id="41310-112">Dans Microsoft Defender for Endpoint, vous pouvez créer des groupes d’appareils et les utiliser pour :</span><span class="sxs-lookup"><span data-stu-id="41310-112">In Microsoft Defender for Endpoint, you can create device groups and use them to:</span></span>
- <span data-ttu-id="41310-113">Limiter l’accès aux alertes et données associées à des groupes d’utilisateurs Azure AD spécifiques avec [des rôles RBAC attribués](rbac.md)</span><span class="sxs-lookup"><span data-stu-id="41310-113">Limit access to related alerts and data to specific Azure AD user groups with [assigned RBAC roles](rbac.md)</span></span> 
- <span data-ttu-id="41310-114">Configurer différents paramètres de correction automatique pour différents ensembles d’appareils</span><span class="sxs-lookup"><span data-stu-id="41310-114">Configure different auto-remediation settings for different sets of devices</span></span>
- <span data-ttu-id="41310-115">Affecter des niveaux de correction spécifiques à appliquer lors d’examens automatisés</span><span class="sxs-lookup"><span data-stu-id="41310-115">Assign specific remediation levels to apply during automated investigations</span></span>
- <span data-ttu-id="41310-116">Dans un examen, filtrez la liste **Appareils** sur des groupes d’appareils spécifiques à l’aide du **filtre** Groupe.</span><span class="sxs-lookup"><span data-stu-id="41310-116">In an investigation, filter the **Devices list** to specific device groups by using the **Group** filter.</span></span>

<span data-ttu-id="41310-117">Vous pouvez créer des groupes d’appareils dans le contexte de l’accès basé sur les rôles (RBAC) pour contrôler qui peut prendre des mesures spécifiques ou voir les informations en attribuant le ou les groupes d’appareils à un groupe d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="41310-117">You can create device groups in the context of role-based access (RBAC) to control who can take specific action or see information by assigning the device group(s) to a user group.</span></span> <span data-ttu-id="41310-118">Pour plus d’informations, voir [Gérer l’accès au portail à l’aide du contrôle d’accès basé sur les rôles.](rbac.md)</span><span class="sxs-lookup"><span data-stu-id="41310-118">For more information, see [Manage portal access using role-based access control](rbac.md).</span></span>

>[!TIP]
> <span data-ttu-id="41310-119">Pour une vue d’ensemble de l’application RBAC, lisez : votre SOC fonctionne-t-il [à plat avec RBAC](https://techcommunity.microsoft.com/t5/Windows-Defender-ATP/Is-your-SOC-running-flat-with-limited-RBAC/ba-p/320015).</span><span class="sxs-lookup"><span data-stu-id="41310-119">For a comprehensive look into RBAC application, read: [Is your SOC running flat with RBAC](https://techcommunity.microsoft.com/t5/Windows-Defender-ATP/Is-your-SOC-running-flat-with-limited-RBAC/ba-p/320015).</span></span>

<span data-ttu-id="41310-120">Dans le cadre du processus de création d’un groupe d’appareils, vous devez :</span><span class="sxs-lookup"><span data-stu-id="41310-120">As part of the process of creating a device group, you'll:</span></span>
- <span data-ttu-id="41310-121">Définissez le niveau de correction automatisé pour ce groupe.</span><span class="sxs-lookup"><span data-stu-id="41310-121">Set the automated remediation level for that group.</span></span> <span data-ttu-id="41310-122">Pour plus d’informations sur les niveaux de correction, voir [Utiliser l’examen automatisé pour examiner et corriger les menaces.](automated-investigations.md)</span><span class="sxs-lookup"><span data-stu-id="41310-122">For more information on remediation levels, see [Use Automated investigation to investigate and remediate threats](automated-investigations.md).</span></span>
- <span data-ttu-id="41310-123">Spécifiez la règle correspondante qui détermine quel groupe d’appareils appartient au groupe en fonction du nom de l’appareil, du domaine, des balises et de la plateforme du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="41310-123">Specify the matching rule that determines which device group belongs to the group based on the device name, domain, tags, and OS platform.</span></span> <span data-ttu-id="41310-124">Si un appareil est également en correspondance avec d’autres groupes, il est ajouté uniquement au groupe d’appareils le plus élevé.</span><span class="sxs-lookup"><span data-stu-id="41310-124">If a device is also matched to other groups, it's added only to the highest ranked device group.</span></span>
- <span data-ttu-id="41310-125">Sélectionnez le groupe d’utilisateurs Azure AD qui doit avoir accès au groupe d’appareils.</span><span class="sxs-lookup"><span data-stu-id="41310-125">Select the Azure AD user group that should have access to the device group.</span></span>
- <span data-ttu-id="41310-126">Classer le groupe d’appareils par rapport aux autres groupes après sa création.</span><span class="sxs-lookup"><span data-stu-id="41310-126">Rank the device group relative to other groups after it's created.</span></span>

>[!NOTE]
><span data-ttu-id="41310-127">Un groupe d’appareils est accessible à tous les utilisateurs si vous n’y affectez aucun groupe Azure AD.</span><span class="sxs-lookup"><span data-stu-id="41310-127">A device group is accessible to all users if you don’t assign any Azure AD groups to it.</span></span>

## <a name="create-a-device-group"></a><span data-ttu-id="41310-128">Créer un groupe d’appareils</span><span class="sxs-lookup"><span data-stu-id="41310-128">Create a device group</span></span>

1. <span data-ttu-id="41310-129">Dans le volet de navigation, sélectionnez **Paramètres**  >  **groupes d’appareils.**</span><span class="sxs-lookup"><span data-stu-id="41310-129">In the navigation pane, select **Settings** > **Device groups**.</span></span>

2. <span data-ttu-id="41310-130">Cliquez **sur Ajouter un groupe d’appareils.**</span><span class="sxs-lookup"><span data-stu-id="41310-130">Click **Add device group**.</span></span>

3. <span data-ttu-id="41310-131">Entrez le nom du groupe et les paramètres d’automatisation et spécifiez la règle correspondante qui détermine quels appareils appartiennent au groupe.</span><span class="sxs-lookup"><span data-stu-id="41310-131">Enter the group name and automation settings and specify the matching rule that determines which devices belong to the group.</span></span> <span data-ttu-id="41310-132">Découvrez [comment l’enquête automatisée démarre.](automated-investigations.md#how-the-automated-investigation-starts)</span><span class="sxs-lookup"><span data-stu-id="41310-132">See [How the automated investigation starts](automated-investigations.md#how-the-automated-investigation-starts).</span></span>

    >[!TIP]
    ><span data-ttu-id="41310-133">Si vous souhaitez grouper des appareils par unité d’organisation, vous pouvez configurer la clé de Registre pour l’affiliation au groupe.</span><span class="sxs-lookup"><span data-stu-id="41310-133">If you want to group devices by organizational unit, you can configure the registry key for the group affiliation.</span></span> <span data-ttu-id="41310-134">Pour plus d’informations sur le marquage des appareils, voir [Créer et gérer des balises d’appareil.](machine-tags.md)</span><span class="sxs-lookup"><span data-stu-id="41310-134">For more information on device tagging, see [Create and manage device tags](machine-tags.md).</span></span>

4. <span data-ttu-id="41310-135">Affichez un aperçu de plusieurs appareils qui seront en correspondance avec cette règle.</span><span class="sxs-lookup"><span data-stu-id="41310-135">Preview several devices that will be matched by this rule.</span></span> <span data-ttu-id="41310-136">Si vous êtes satisfait de la règle, cliquez sur **l’onglet Accès** utilisateur.</span><span class="sxs-lookup"><span data-stu-id="41310-136">If you're satisfied with the rule, click the **User access** tab.</span></span>

5. <span data-ttu-id="41310-137">Affectez les groupes d’utilisateurs qui peuvent accéder au groupe d’appareils que vous avez créé.</span><span class="sxs-lookup"><span data-stu-id="41310-137">Assign the user groups that can access the device group you created.</span></span>

    >[!NOTE]
    ><span data-ttu-id="41310-138">Vous pouvez uniquement accorder l’accès aux groupes d’utilisateurs Azure AD affectés à des rôles RBAC.</span><span class="sxs-lookup"><span data-stu-id="41310-138">You can only grant access to Azure AD user groups that have been assigned to RBAC roles.</span></span>

6. <span data-ttu-id="41310-139">Cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="41310-139">Click **Close**.</span></span> <span data-ttu-id="41310-140">Les modifications de configuration sont appliquées.</span><span class="sxs-lookup"><span data-stu-id="41310-140">The configuration changes are applied.</span></span>

## <a name="manage-device-groups"></a><span data-ttu-id="41310-141">Gérer les groupes d’appareils</span><span class="sxs-lookup"><span data-stu-id="41310-141">Manage device groups</span></span>

<span data-ttu-id="41310-142">Vous pouvez promouvoir ou rétrograder le rang d’un groupe d’appareils afin qu’il soit plus ou moins prioritaire lors de la mise en correspondance.</span><span class="sxs-lookup"><span data-stu-id="41310-142">You can promote or demote the rank of a device group so that it's given higher or lower priority during matching.</span></span> <span data-ttu-id="41310-143">Lorsqu’un appareil est en correspondance avec plusieurs groupes, il est ajouté uniquement au groupe le plus élevé.</span><span class="sxs-lookup"><span data-stu-id="41310-143">When a device is matched to more than one group, it's added only to the highest ranked group.</span></span> <span data-ttu-id="41310-144">Vous pouvez également modifier et supprimer des groupes.</span><span class="sxs-lookup"><span data-stu-id="41310-144">You can also edit and delete groups.</span></span>



>[!WARNING]
><span data-ttu-id="41310-145">La suppression d’un groupe d’appareils peut affecter les règles de notification par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="41310-145">Deleting a device group may affect email notification rules.</span></span> <span data-ttu-id="41310-146">Si un groupe d’appareils est configuré sous une règle de notification par courrier électronique, il sera supprimé de cette règle.</span><span class="sxs-lookup"><span data-stu-id="41310-146">If a device group is configured under an email notification rule, it will be removed from that rule.</span></span> <span data-ttu-id="41310-147">Si le groupe d’appareils est le seul groupe configuré pour une notification par courrier électronique, cette règle de notification par courrier électronique est supprimée avec le groupe d’appareils.</span><span class="sxs-lookup"><span data-stu-id="41310-147">If the device group is the only group configured for an email notification, that email notification rule will be deleted along with the device group.</span></span>

<span data-ttu-id="41310-148">Par défaut, les groupes d’appareils sont accessibles à tous les utilisateurs ayant accès au portail.</span><span class="sxs-lookup"><span data-stu-id="41310-148">By default, device groups are accessible to all users with portal access.</span></span> <span data-ttu-id="41310-149">Vous pouvez modifier le comportement par défaut en attribuant des groupes d’utilisateurs Azure AD au groupe d’appareils.</span><span class="sxs-lookup"><span data-stu-id="41310-149">You can change the default behavior by assigning Azure AD user groups to the device group.</span></span>

<span data-ttu-id="41310-150">Les appareils qui ne correspondent à aucun groupe sont ajoutés au groupe Appareils non regroupés (par défaut).</span><span class="sxs-lookup"><span data-stu-id="41310-150">Devices that aren't matched to any groups are added to Ungrouped devices (default) group.</span></span> <span data-ttu-id="41310-151">Vous ne pouvez pas modifier le rang de ce groupe ni le supprimer.</span><span class="sxs-lookup"><span data-stu-id="41310-151">You cannot change the rank of this group or delete it.</span></span> <span data-ttu-id="41310-152">Toutefois, vous pouvez modifier le niveau de correction de ce groupe et définir les groupes d’utilisateurs Azure AD qui peuvent accéder à ce groupe.</span><span class="sxs-lookup"><span data-stu-id="41310-152">However, you can change the remediation level of this group, and define the Azure AD user groups that can access this group.</span></span>

>[!NOTE]
> <span data-ttu-id="41310-153">L’application de modifications à la configuration du groupe d’appareils peut prendre jusqu’à plusieurs minutes.</span><span class="sxs-lookup"><span data-stu-id="41310-153">Applying changes to device group configuration may take up to several minutes.</span></span>


### <a name="add-device-group-definitions"></a><span data-ttu-id="41310-154">Ajouter des définitions de groupe d’appareils</span><span class="sxs-lookup"><span data-stu-id="41310-154">Add device group definitions</span></span>
<span data-ttu-id="41310-155">Les définitions de groupe d’appareils peuvent également inclure plusieurs valeurs pour chaque condition.</span><span class="sxs-lookup"><span data-stu-id="41310-155">Device group definitions can also include multiple values for each condition.</span></span> <span data-ttu-id="41310-156">Vous pouvez définir plusieurs balises, noms d’appareils et domaines sur la définition d’un seul groupe d’appareils.</span><span class="sxs-lookup"><span data-stu-id="41310-156">You can set multiple tags, device names, and domains to the definition of a single device group.</span></span>

1. <span data-ttu-id="41310-157">Créez un groupe d’appareils, puis sélectionnez **Onglet** Appareils.</span><span class="sxs-lookup"><span data-stu-id="41310-157">Create a new device group, then select **Devices** tab.</span></span>
2. <span data-ttu-id="41310-158">Ajoutez la première valeur pour l’une des conditions.</span><span class="sxs-lookup"><span data-stu-id="41310-158">Add the first value for one of the conditions.</span></span>
3. <span data-ttu-id="41310-159">Sélectionnez `+` pour ajouter d’autres lignes du même type de propriété.</span><span class="sxs-lookup"><span data-stu-id="41310-159">Select `+` to add more rows of the same property type.</span></span>

>[!TIP]
> <span data-ttu-id="41310-160">Utilisez l’opérateur « OR » entre les lignes du même type de condition, qui autorise plusieurs valeurs par propriété.</span><span class="sxs-lookup"><span data-stu-id="41310-160">Use the 'OR' operator between rows of the same condition type, which allows multiple values per property.</span></span>
> <span data-ttu-id="41310-161">Vous pouvez ajouter jusqu’à 10 lignes (valeurs) pour chaque type de propriété : balise, nom de l’appareil, domaine.</span><span class="sxs-lookup"><span data-stu-id="41310-161">You can add up to 10 rows (values) for each property type - tag, device name, domain.</span></span>

<span data-ttu-id="41310-162">Pour plus d’informations sur la liaison aux définitions de groupes d’appareils, voir Groupes d’appareils [- Microsoft 365 sécurité.](https://sip.security.microsoft.com/homepage)</span><span class="sxs-lookup"><span data-stu-id="41310-162">For more information on linking to device groups definitions, see [Device groups - Microsoft 365 security](https://sip.security.microsoft.com/homepage).</span></span>

## <a name="related-topics"></a><span data-ttu-id="41310-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41310-163">Related topics</span></span>

- [<span data-ttu-id="41310-164">Gérer l’accès au portail à l’aide du contrôle d’accès basé sur un rôle</span><span class="sxs-lookup"><span data-stu-id="41310-164">Manage portal access using role-based based access control</span></span>](rbac.md)
- [<span data-ttu-id="41310-165">Créer et gérer des balises d’appareils</span><span class="sxs-lookup"><span data-stu-id="41310-165">Create and manage device tags</span></span>](machine-tags.md)
- [<span data-ttu-id="41310-166">Obtenir la liste des groupes d’appareils client à l’aide Graph API</span><span class="sxs-lookup"><span data-stu-id="41310-166">Get list of tenant device groups using Graph API</span></span>](/graph/api/device-list-memberof)
