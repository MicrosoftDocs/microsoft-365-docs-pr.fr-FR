---
title: 'Conditions préalables & autorisations : gestion des menaces et des vulnérabilités'
description: Avant de commencer à utiliser la gestion des menaces et des vulnérabilités, assurez-vous que vous avez les configurations et autorisations pertinentes.
keywords: conditions préalables & gestion des menaces et des vulnérabilités, conditions préalables pour la gestion des menaces et des vulnérabilités, conditions préalables pour les autorisations TVM MDATP, gestion des vulnérabilités
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: dansimp
author: dansimp
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: 1d9c3233f72541ccd0463eefef93bde5e7d9900f
ms.sourcegitcommit: 582555d2b4ef5f2e2494ffdeab2c1d49e5d6b724
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51499960"
---
# <a name="prerequisites--permissions---threat-and-vulnerability-management"></a><span data-ttu-id="d692d-104">Conditions préalables & autorisations : gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="d692d-104">Prerequisites & permissions - threat and vulnerability management</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="d692d-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="d692d-105">**Applies to:**</span></span>

- [<span data-ttu-id="d692d-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="d692d-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="d692d-107">Gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="d692d-107">Threat and vulnerability management</span></span>](next-gen-threat-and-vuln-mgt.md)
- [<span data-ttu-id="d692d-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="d692d-108">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="d692d-109">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="d692d-109">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="d692d-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="d692d-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-portaloverview-abovefoldlink)

<span data-ttu-id="d692d-111">Assurez-vous que vos appareils :</span><span class="sxs-lookup"><span data-stu-id="d692d-111">Ensure that your devices:</span></span>

- <span data-ttu-id="d692d-112">Sont intégrés à Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="d692d-112">Are onboarded to Microsoft Defender for Endpoint</span></span>
- <span data-ttu-id="d692d-113">Exécuter les [systèmes d’exploitation et les plateformes pris en charge](tvm-supported-os.md)</span><span class="sxs-lookup"><span data-stu-id="d692d-113">Run [supported operating systems and platforms](tvm-supported-os.md)</span></span>
- <span data-ttu-id="d692d-114">Installez et déployez les mises à jour obligatoires suivantes dans votre réseau pour augmenter les taux de détection de l’évaluation des vulnérabilités :</span><span class="sxs-lookup"><span data-stu-id="d692d-114">Have the following mandatory updates installed and deployed in your network to boost your vulnerability assessment detection rates:</span></span>

> <span data-ttu-id="d692d-115">Version</span><span class="sxs-lookup"><span data-stu-id="d692d-115">Release</span></span> | <span data-ttu-id="d692d-116">Numéro et lien de la mise à jour de sécurité de la KB</span><span class="sxs-lookup"><span data-stu-id="d692d-116">Security update KB number and link</span></span>
> :---|:---
> <span data-ttu-id="d692d-117">Windows 10 version 1709</span><span class="sxs-lookup"><span data-stu-id="d692d-117">Windows 10 Version 1709</span></span> | <span data-ttu-id="d692d-118">[KB4493441 et](https://support.microsoft.com/help/4493441/windows-10-update-kb4493441) [KB 4516071](https://support.microsoft.com/help/4516071/windows-10-update-kb4516071)</span><span class="sxs-lookup"><span data-stu-id="d692d-118">[KB4493441](https://support.microsoft.com/help/4493441/windows-10-update-kb4493441) and [KB 4516071](https://support.microsoft.com/help/4516071/windows-10-update-kb4516071)</span></span>
> <span data-ttu-id="d692d-119">Windows 10 version 1803</span><span class="sxs-lookup"><span data-stu-id="d692d-119">Windows 10 Version 1803</span></span> | <span data-ttu-id="d692d-120">[KB4493464 et](https://support.microsoft.com/help/4493464) [KB 4516045](https://support.microsoft.com/help/4516045/windows-10-update-kb4516045)</span><span class="sxs-lookup"><span data-stu-id="d692d-120">[KB4493464](https://support.microsoft.com/help/4493464) and [KB 4516045](https://support.microsoft.com/help/4516045/windows-10-update-kb4516045)</span></span>
> <span data-ttu-id="d692d-121">Windows 10 Version 1809</span><span class="sxs-lookup"><span data-stu-id="d692d-121">Windows 10 Version 1809</span></span> | [<span data-ttu-id="d692d-122">KB 4516077</span><span class="sxs-lookup"><span data-stu-id="d692d-122">KB 4516077</span></span>](https://support.microsoft.com/help/4516077/windows-10-update-kb4516077)
> <span data-ttu-id="d692d-123">Windows 10 version 1903</span><span class="sxs-lookup"><span data-stu-id="d692d-123">Windows 10 Version 1903</span></span> | [<span data-ttu-id="d692d-124">KB 4512941</span><span class="sxs-lookup"><span data-stu-id="d692d-124">KB 4512941</span></span>](https://support.microsoft.com/help/4512941/windows-10-update-kb4512941)

- <span data-ttu-id="d692d-125">Sont intégrés à [Microsoft Intune](https://docs.microsoft.com/mem/intune/fundamentals/what-is-intune) et  [Microsoft Endpoint Configuration Manager](https://docs.microsoft.com/mem/configmgr/protect/deploy-use/endpoint-protection-configure) pour vous aider à résoudre les menaces trouvées par la gestion des menaces et des vulnérabilités.</span><span class="sxs-lookup"><span data-stu-id="d692d-125">Are onboarded to [Microsoft Intune](https://docs.microsoft.com/mem/intune/fundamentals/what-is-intune) and  [Microsoft Endpoint Configuration Manager](https://docs.microsoft.com/mem/configmgr/protect/deploy-use/endpoint-protection-configure) to help remediate threats found by threat and vulnerability management.</span></span> <span data-ttu-id="d692d-126">Si vous utilisez Configuration Manager, mettez à jour votre console vers la dernière version.</span><span class="sxs-lookup"><span data-stu-id="d692d-126">If you're using Configuration Manager, update your console to the latest version.</span></span>
    - <span data-ttu-id="d692d-127">**Remarque**: si la connexion Intune est activée, vous pouvez créer une tâche de sécurité Intune lors de la création d’une demande de correction.</span><span class="sxs-lookup"><span data-stu-id="d692d-127">**Note**: If you have the Intune connection enabled, you get an option to create an Intune security task when creating a remediation request.</span></span> <span data-ttu-id="d692d-128">Cette option n’apparaît pas si la connexion n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="d692d-128">This option does not appear if the connection is not set.</span></span>
- <span data-ttu-id="d692d-129">Avoir au moins une recommandation de sécurité qui peut être vue dans la page de l’appareil</span><span class="sxs-lookup"><span data-stu-id="d692d-129">Have at least one security recommendation that can be viewed in the device page</span></span>
- <span data-ttu-id="d692d-130">Sont marqués ou marqués comme co-gérés</span><span class="sxs-lookup"><span data-stu-id="d692d-130">Are tagged or marked as co-managed</span></span>

## <a name="relevant-permission-options"></a><span data-ttu-id="d692d-131">Options d’autorisation pertinentes</span><span class="sxs-lookup"><span data-stu-id="d692d-131">Relevant permission options</span></span>

1. <span data-ttu-id="d692d-132">Connectez-vous au Centre de sécurité Microsoft Defender à l’aide d’un compte attribué par un administrateur de sécurité ou un rôle d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="d692d-132">Log in to Microsoft Defender Security Center using account with a Security administrator or Global administrator role assigned.</span></span>
2. <span data-ttu-id="d692d-133">Dans le volet de navigation, sélectionnez **Paramètres > rôles.**</span><span class="sxs-lookup"><span data-stu-id="d692d-133">In the navigation pane, select **Settings > Roles**.</span></span>

<span data-ttu-id="d692d-134">Pour plus d’informations, voir [Créer et gérer des rôles pour le contrôle d’accès basé sur les rôles](user-roles.md)</span><span class="sxs-lookup"><span data-stu-id="d692d-134">For more information, see [Create and manage roles for role-based access control](user-roles.md)</span></span>

### <a name="view-data"></a><span data-ttu-id="d692d-135">Afficher les données</span><span class="sxs-lookup"><span data-stu-id="d692d-135">View data</span></span>

- <span data-ttu-id="d692d-136">**Opérations de sécurité** : afficher toutes les données des opérations de sécurité dans le portail</span><span class="sxs-lookup"><span data-stu-id="d692d-136">**Security operations** - View all security operations data in the portal</span></span>
- <span data-ttu-id="d692d-137">**Gestion des menaces et des vulnérabilités** : afficher les données de gestion des menaces et des vulnérabilités dans le portail</span><span class="sxs-lookup"><span data-stu-id="d692d-137">**Threat and vulnerability management** - View threat and vulnerability management data in the portal</span></span>

### <a name="active-remediation-actions"></a><span data-ttu-id="d692d-138">Actions de correction actives</span><span class="sxs-lookup"><span data-stu-id="d692d-138">Active remediation actions</span></span>

- <span data-ttu-id="d692d-139">**Opérations de sécurité** : prendre des mesures de réponse, approuver ou ignorer les actions de correction en attente, gérer les listes autorisées/bloquées pour l’automatisation et les indicateurs</span><span class="sxs-lookup"><span data-stu-id="d692d-139">**Security operations** - Take response actions, approve or dismiss pending remediation actions, manage allowed/blocked lists for automation and indicators</span></span>
- <span data-ttu-id="d692d-140">**Gestion des menaces et des vulnérabilités : gestion des exceptions** : créer des exceptions et gérer les exceptions actives</span><span class="sxs-lookup"><span data-stu-id="d692d-140">**Threat and vulnerability management - Exception handling** - Create new exceptions and manage active exceptions</span></span>
- <span data-ttu-id="d692d-141">**Gestion des menaces et des vulnérabilités : gestion** des corrections : soumettre de nouvelles demandes de correction, créer des tickets et gérer les activités de correction existantes</span><span class="sxs-lookup"><span data-stu-id="d692d-141">**Threat and vulnerability management - Remediation handling** - Submit new remediation requests, create tickets, and manage existing remediation activities</span></span>

<span data-ttu-id="d692d-142">Pour plus d’informations, voir [les options d’autorisation RBAC](user-roles.md#permission-options)</span><span class="sxs-lookup"><span data-stu-id="d692d-142">For more information, see [RBAC permission options](user-roles.md#permission-options)</span></span>

## <a name="related-articles"></a><span data-ttu-id="d692d-143">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="d692d-143">Related articles</span></span>

- [<span data-ttu-id="d692d-144">Vue d’ensemble de la gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="d692d-144">Threat and vulnerability management overview</span></span>](next-gen-threat-and-vuln-mgt.md)
- [<span data-ttu-id="d692d-145">Plateformes et systèmes d’exploitation pris en charge</span><span class="sxs-lookup"><span data-stu-id="d692d-145">Supported operating systems and platforms</span></span>](tvm-supported-os.md)
- [<span data-ttu-id="d692d-146">Affecter une valeur aux appareils</span><span class="sxs-lookup"><span data-stu-id="d692d-146">Assign device value</span></span>](tvm-assign-device-value.md)
- [<span data-ttu-id="d692d-147">Tableau de bord de gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="d692d-147">Threat and vulnerability management dashboard</span></span>](tvm-dashboard-insights.md)

